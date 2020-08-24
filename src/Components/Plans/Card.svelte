<style>

.card{
    width: 100%;
    border-radius: 20px;
    min-height: 50vh;
    display: flex;
    flex-direction: column;
    background-color: #f3f3f3;
    /* background: linear-gradient(to bottom, #ffffff 1%,#fafafa 100%,#f3f3f3 100%); */
    justify-content: space-between;
    transition: all .3s ease;
}

.card:hover{
    transform: scale(1.1);
}

.card-title{
    margin-bottom: 10px;
}

.card-cost h3{
    display: inline-block;
}

.card-list{
    padding: 0 20px 8px 20px;
}

.card-list p{
    font-size: 14px;
}

hr{
    border: 3px solid var(--primary);
    margin: 10px auto 20px auto;
}

 @media screen and (max-width:768px){ 
    /* .card-list{
        padding: 0;
    } */ 
    
    h3{
        font-size: 30px !important;
    }
}

</style>

<script>
    import {showModal, planModal} from '../../Store/store.js';
    import ButonAction from '../Shared/BotonAction.svelte';

    export let title;
    export let cost;
    export let boton;
    export let description;

    function handleMessage(){
        showModal.update(n => {
            return !$showModal;
        })

        planModal.update(n => {
            return title;
        })
    }

</script>


<div class="card wrapper shadow">

    <div class="card-content-top">
        <div class="card-title">
            <h3>{title}</h3>
        </div>
    
        <div class="card-cost">
            <span>desde</span>
            <h3>{cost} Soles</h3>
                
            <hr>
        </div>
    
    
        <div class="card-list">
            {#each description as desc}
                <p>{desc}</p>
            {/each}
        </div>
    </div>

    <div class="card-button-action">
        <ButonAction text={boton} on:click={handleMessage}/>     
    </div>

</div>

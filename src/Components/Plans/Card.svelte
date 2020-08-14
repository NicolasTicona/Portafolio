<style>

.card-info{
    width: 100%;
    border-radius: 20px;

    min-height: 50vh;
    display: flex;
    flex-direction: column;
    background-color: rgba(255, 255, 255, .8);
    justify-content: space-between;
    transition: all .3s ease;
}

.card-info:hover{
    transform: scale(1.1);
}

.card-title{
    margin-bottom: 10px;
}

.cost h3{
    display: inline-block;
}

hr{
    border: 3px solid var(--primary);
    margin: 10px auto 20px auto;
}

ul{
    margin-left: 20px;
    text-align: left;
}


</style>

<script>
    import {showModal} from '../../Store/store.js';
    import ButonAction from '../Shared/BotonAction.svelte';

    export let title;
    export let cost;
    export let boton;
    export let description;

    function handleMessage(){
        console.log('que fu')
        showModal.update(n => {
            return !$showModal;
        })
    }

</script>


<div class="card-info wrapper shadow">

    <div class="top-content">
        <div class="card-title">
            <h3>{title}</h3>
        </div>
    
        <div class="cost">
            <span>desde</span>
            <h3>{cost} Soles</h3>
                
            <hr>
        </div>
    
    
        <ul>
            {#each description as desc}
                <li>{desc}</li>
            {/each}
        </ul>
    </div>

    <div class="button-action">
        <ButonAction text={boton} on:click={handleMessage}/>     
    </div>

</div>

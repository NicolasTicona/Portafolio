<style>

    .card{
        width: 100%;
        border-radius: 20px;
        min-height: 50vh;
        display: flex;
        flex-direction: column;
        background-color: var(--secondary);
        /* background: linear-gradient(to bottom, #ffffff 1%,#fafafa 100%,#f3f3f3 100%); */
        justify-content: space-between;
        transition: all .3s ease;
        text-align: center;
    }

    .dark{
        background-color: var(--primary) !important;
        color: #fff !important;
    }

    .card:hover{
        transform: scale(1.03);
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
        font-size: 18px;
    }

    hr{
        border: 3px solid var(--primary);
        margin: 10px auto 20px auto;
    }

    .card-button-action{
        margin-top: 30px;
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
    export let asesoria;

    function handleMessage(){
        showModal.update(n => {
            return !$showModal;
        })

        planModal.update(n => {
            return title;
        })
    }

</script>


<div class="card wrapper shadow {asesoria ? 'dark': ''} ">

    <div class="card-content-top">
        <div class="card-title">
            <h3>{title}</h3>
        </div>
    
        {#if cost}
            <div class="card-cost">
                <span>desde</span>
                <h3>{cost} Soles</h3>
                    
                <hr>
            </div>
        {/if}
    
    
        <div class="card-list">
            {#each description as desc}
                <p>{@html desc}</p>
            {/each}
        </div>
    </div>

    <div class="card-button-action">
        <ButonAction 
            text={boton} 
            on:click={handleMessage}/>     
    </div>

</div>

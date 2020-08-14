<style>

    .modal{
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        background-color: rgba(0, 0, 0, .7);
        z-index: 10;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .modal-content{
        width: 40%;
        margin: auto;
        background-color: var(--secondary);
        border-radius: 20px;
    }

    .modal-info{
        font-size: 12px;
        font-weight: bold;
        margin-bottom: 10px;
    }
    input, select{
        border-radius: 5px;
        width: 100%;
    }

    a{
        display: block;
        margin-top: 10px;
        background-color: var(--primary);
        border-radius: 10px;
        text-align: center;
        color: #fff;
        padding: 10px;
        text-decoration: none;
    }

    .modal-close button{
        border: none;
        font-weight: bold;
        cursor: pointer;
        font-size: 20px;
        color: var(--primary);
    }

    .modal-message-error{
        font-size: 10px;
        color: red;
        margin-top: 8px;
    }

</style>

<script>

    import {showModal} from '../../Store/store.js';
    import {onMount} from 'svelte'
    import {fade} from 'svelte/transition';


    let countries = [];
    onMount(async () => {
        const res = await fetch('https://gist.githubusercontent.com/Goles/3196253/raw/9ca4e7e62ea5ad935bb3580dc0a07d9df033b451/CountryCodes.json');
        countries = await res.json();
    })  


    let name  = '';
    let phone = '999999999';
    let email = 'example@gmail.com';
    let anexo = '+51'
    let contact_info = '';
    let showPhoneError = false;

    $: if(name && phone && anexo){
        handleSend();
    }

    function handleSend(){

        if(phone.trim().length != 9){
            showPhoneError = true;
            return;
        }

        showPhoneError = false;
        if(name.trim().length > 0 && phone.trim().length > 0){
            contact_info = `https://api.whatsapp.com/send?phone=51902376118&text=Hola!%20Soy%20${name}%20me%20gustar%C3%ADa%20hablar%20contigo%`
            contact_info += `20este%20es%20mi%20numero%20${anexo}${phone}`;
            if(email) contact_info += `%20y%20este%20es%20mi%20correo%20${email}`;
        }
    }

    function handleClose(){
        showModal.update(n => {
            return false
        })
    }

</script>

<div class="modal" transition:fade>
    <div class="modal-content wrapper">
        <div class="modal-close">
            <button on:click={handleClose}>X</button>
        </div>

        <p class="modal-info">Este mensaje será enviado a mi Whatssap Personal. La respuesta sera en un lapso máximo de 2 horas</p>

        <form>
            <input bind:value={name} type="text" placeholder="Tu nombre">
            {#if countries && countries.length > 0}
                <select bind:value={anexo}>
                    {#each countries as country}
                        <option value={country.dial_code}>{country.name}</option>
                        <p>Cargando código de país...</p>
                    {/each}
                </select>
            {:else}
                <p>Cargando códigos...</p>
            {/if}
            {#if showPhoneError}
                <span class="modal-message-error">Número de celular inválido</span>
            {/if}
            <input bind:value={phone} type="text" placeholder="Tu número de celular">
            <input bind:value={email} type="email" placeholder="Tu correo electrónico">

            {#if name && phone && !showPhoneError}
                <a href={contact_info} target="_blank">Enviar</a>
            {/if}
        </form>
    </div>
</div>
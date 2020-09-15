<style>

    .quote{
        color: #fff;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
    }

    .quote-image a{ display: inline-block;}
    .quote-image img{
        display: inline-block;
        width: 50px;
        height: 50px;
        background: #fff;
        border-radius: 50%;
    }

    .quote-description{
        margin-left: 8px;
        color: #fff;
    }

    .quote-description h5{
        display: inline-block;
    }

    .quote-description p{
        margin-top: 5px;
        font-size: 12px;
        font-weight: normal;
        font-style: italic;
        background-color: #fff;
        color: var(--primary);
        border-radius: 10px 10px 20px 10px;
        padding: 10px;
        font-weight: bold;
    }

    .quote-link{
        display: inline-block;
    }

    .quote-link img{
        width: 10px;
        vertical-align: middle;
    }
    
    .quote-description span{
        display: inline-block;
        font-weight: bold;
        margin-top: 6px;
    }

</style>

<script>
    
    export let name;
    export let rol;
    export let desc;
    export let img;
    export let link;

</script>

<div class="quote">
    <div class="quote-image">

        {#if link}
            <a href={link} target="_blank">
                <img src={img} alt="Imágen">
            </a>
        {:else}
            <img src={img} alt="Imágen">
        {/if}

    </div>

    <div class="quote-description">
        <h5>{name}</h5>
        {#if link}
            <a class="quote-link" href={link} target="_blank">
                <img src="/assets/networks/linkedin.png" alt="Linkedin">
            </a>
        {/if}
        <br>
        <span>{rol}</span>
        <p class="shadow">{desc}</p>
    </div>
</div>
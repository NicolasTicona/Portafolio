<style>

    .quote{
        color: #fff;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
    }

    .quote-image .image{
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
    
    .quote-description span{
        display: block;
        font-weight: bold;
        font-size: 10px;
        margin-top: 6px;
    }

</style>

<script>
    
    export let name;
    export let rol;
    export let desc;
    export let img;

</script>

<div class="quote">
    <div class="quote-image">
        <img src={img} alt="Imágen" class="image">
    </div>

    <div class="quote-description">
        <h5>{name}</h5>
        <span>{rol}</span>
        <p class="shadow">{desc}</p>
    </div>
</div>
<style>

    a{
        text-decoration: none;
        display: inline-block;
        background-color: var(--primary);
        min-width: 200px;
        text-align: center;
        color: #fff;
        font-weight: bold;
        border-radius: 30px;
        border: none;
        padding: 15px 10px;
        cursor: pointer;
    }
    .up{
        border: 3px solid var(--primary);
        background: #fff;
        color: var(--primary)
    }

    
</style>

<script>
    export let text;
    export let up;
    export let scroll;
</script>

<a on:click href={scroll} class="{up === true ? 'up shadow' : 'shadow'}">
    {text}
</a>
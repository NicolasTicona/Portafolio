<style>

    button{
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

    button:active{
        background-color: var(--primary);
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
</script>

<button on:click class="{up === true ? 'up shadow' : 'shadow'}">
    {text}
</button>
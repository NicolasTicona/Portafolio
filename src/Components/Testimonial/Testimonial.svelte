<style>

    .testimonial{
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .testimonial-quote{
        width: 40%;
        margin: auto;
        margin-bottom: 20px;
    }
    
    @media screen and (max-width:768px){
        .testimonial-quote{
            width: 70%;
        }
    }

</style>

<script>
    import Quote from './Quote.svelte';

</script>

<div class="testimonial">
    <div class="testimonial-quote">
        <Quote />
    </div>
    <div class="testimonial-quote">
        <Quote />
    </div>
    <div class="testimonial-quote">
        <Quote />
    </div>
</div>
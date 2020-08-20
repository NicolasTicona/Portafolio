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
import Modal from '../Modal/Modal.svelte';

    let testimonio1 = {
        name : 'Marco Flores',
        rol  : 'COO de Smiledu',
        desc : 'Excelente como persona y profesional. Responsable y comprometido.',
        img  : '/assets/marco-flores.jfif'
    }


    let testimonio2 = {
        name : 'Diego Flores',
        rol  : 'CEO de Smiledu',
        desc : 'Gran crecimiento y adaptación en el equipo. Proactivo y profesional.',
        img  : '/assets/diego-flores.jfif'
    }


    let testimonio3 = {
        name : 'Gerardo Portilla',
        rol  : 'Director del Centro David',
        desc : 'Responsable y muy profesional. Gran crecimiento y adaptación en el equipo.',
        img  : '/assets/gerardo-portilla.jpg'
    }

</script>

<div class="testimonial">
    <div class="testimonial-quote">
        <Quote {...testimonio1} />
    </div>
    <div class="testimonial-quote">
        <Quote {...testimonio2}/>
    </div>
    <div class="testimonial-quote">
        <Quote {...testimonio3}/>
    </div>
</div>
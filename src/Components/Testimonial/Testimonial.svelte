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

    let testimonio1 = {
        name : 'Marco Flores',
        rol  : 'Founder de Smiledu',
        link : 'https://www.linkedin.com/in/marco-antonio-flores-gonzales-8217b38b/',
        desc : 'Excelente como persona y profesional. Responsable y comprometido.',
        img  : '/assets/marco-flores.jfif'
    }


    let testimonio2 = {
        name : 'Diego Flores',
        rol  : 'Founder de Smiledu',
        link : 'https://www.linkedin.com/in/diego-flores-gonzales-45a75069/',
        desc : 'Gran crecimiento y adaptación en el equipo. Proactivo y profesional.',
        img  : '/assets/diego-flores.jfif'
    }


    let testimonio3 = {
        name : 'Gerardo Portilla',
        rol  : 'Director del Centro de Salud Mental David',
        desc : 'Un trabajo profesional de alta calidad, con alta funcionalidad y cumple al pie de la letra lo estipulado en su proforma.',
        img  : '/assets/gerardo-portilla.jpg',
        link : false
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
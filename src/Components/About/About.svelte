<style>

    .about{
        background-color: var(--secondary);
        text-align: center;
    }

    .about-description{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }

    /* .about-image-round{
        width: 200px;
        border-radius: 50%;
        border: 3px solid var(--primary)
    } */

    .about-description p{
        width: 40%;
    }

    @media screen and (max-width:768px){
        .about {text-align: center}
        .about-description{justify-content: center}

        .about-description p{
            width: 90%;
            margin-top: 10px;
        }
    }

</style>

<script>

</script>

<div class="about wrapper">
    <div class="about-container wrapper">
        <h2 class="about-title">Sobre mí</h2>
        <div class="about-description">
            <!-- <img class="about-image-round" src="/assets/Nicolas.jpg" alt="Nicolas Ticona Valdivia"> -->
            <p>
                Me dedico a la programación desde hace 5 años. He aprendido haciendo varios proyectos y también contribuyendo a la comunidad.
                He participado en varios eventos como <a target="_blank" href="https://www.belatrixsf.com/hackatrix/2019_lima/">Hackatrix 2019</a>, la <a targe="_blank" href="https://olimpiadadeinformatica.org.pe/">OPI</a> y la <a target="_blank" href="https://www.oei.es/historico/ciic.htm">CIIC</a> . Me fascina en todos los aspectos el desarrollo de aplicaciones 
                y como evolucionan las tecnologías que te ayudan con esto.
            </p>
        </div>
    </div>
</div>
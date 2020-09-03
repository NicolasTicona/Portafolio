<style>
    .plans{
        padding: 100px 0 200px 0;
        margin-top: 0;
        background-color: var(--secondary);
        background-image: url('/assets/body-bg.svg');
        background-size: cover;
    }
    
    .plans-info-top{
        text-align: left;
        margin-left: 20px;
    }

    span{
        font-size: 12px;
    }

    .plans-cards{
        /* background-color: #ccc; */
        margin: 20px;
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        align-items: center;
        flex-wrap: wrap;
    }

    .plans-card{
        width: 35%;
        margin: 10px;
    }

    /* .plans-card:nth-child(2){
        margin-top: 50px;
    } */

    @media screen and (max-width:768px){

        .plans-cards{
            justify-content: center;
        }

        .plans-info-top{
            margin: 20px;
            text-align: center;
        }
        .plans-card{
            width: 90%;
            margin: 20px 0;
        }

        .plans-info-top{
            padding: 0 20px;
        }
    }

</style>

<script>

    import Card from './Card.svelte';

    // let basicPlan = {
    //     title: 'Básico',
    //     cost : 229,
    //     description: [
    //         'El plan perfecto para empezar y tener presencia en internet',
    //         '¿Qué tal si creamos tu portafolio de proyectos, la página web de tu negocio, o una tienda online para empezar a vender?'
    //     ],
    //     boton: 'Lo quiero!',
    //     asesoria: false
    // };

    let asesoria = {
        title: 'Asesoria Gratis',
        description: [
            '¿Sabes que es un <b>dominio</b>, un <b>hosting</b> o que se necesita para llevar a cabo tu <b>sitio web</b>?',
            '¡Accede a una <b>asesoria totalmente gratis</b>!',
            'Solo haz click en este botón'
        ],
        boton: 'Vamos!',
        asesoria: true
    };

    let proPlan = {
        title: 'Emprendedor',
        cost: 529,
        description: [
            '¡No puedes quedarte atrás!',
            'Es hora de crear tu <b>portafolio profesional</b>, el sitio web perfecto para tu <b>empresa</b> o la construcción de una marca para <b>presencia web</b>.' 
        ],
        boton: 'Empecemos!',
        asesoria: false
    };
    
    // let appPlan = {
    //     title: 'Profesional',
    //     cost: 1299,
    //     description: [
    //         '¿Tienes una idea increíble?',
    //         '¿Necesitas integrar muchas funcionalidades dentro de una plataforma?',
    //         'Despeguemos ese proyecto al siguiente nivel'
    //     ],
    //     boton: 'Hablemos!'
    // };

</script>

<div class="plans wrapper" id="scroll-plans">

    <div class="plans-info-top">
        <h2 id="scroll-planes">Trabajemos juntos</h2>
        <h4>Adquiere el mejor plan para tu sitio web</h4>
        <span>*No incluye costos de Hosting & Dominio</span>
        <br>
        <span>*No incluye IGV</span>
    </div>

    <div class="plans-cards">
        <div class="plans-card">
            <Card 
                {...proPlan}
            />
        </div>

       <div class="plans-card">
            <Card 
                {...asesoria}
            />
        </div>

        <!-- <div class="plans-card">
            <Card 
                {...appPlan}
            />
        </div> -->

    </div>

</div>

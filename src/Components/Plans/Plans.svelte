<style>
    .plans{
        padding: 100px 0 200px 0;
        text-align: center;
        margin-top: 0;
        background-image: url('/assets/body-bg.svg');
        background-size: cover;
    }
    
    .plans-info-top{
        text-align: center;
    }

    span{
        font-size: 15px;
    }

    .plans-cards{
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        flex-wrap: wrap;
    }

    .plans-card{
        width: 25%;
    }

    .plans-card:nth-child(2){
        margin-top: 50px;
    }


</style>

<script>

    import Card from './Card.svelte';

    let basicPlan = {
        title: 'Básico',
        cost : 229,
        description: [
            'Portafolio de trabajo', 'Páginas web informativas',
            'Negocios pequeños', 'Presencia online',
            'Tienda online'
        ],
        boton: 'Lo quiero!'
    };

    let proPlan = {
        title: 'Profesional',
        cost: 529,
        description: [
            'Landing Page', 'Construcción de Marca',
            'Negocios medianos - grandes',
            'Campañas'
        ],
        boton: 'Empecemos!'
    };

    let appPlan = {
        title: 'Plataforma Web',
        cost: 999,
        description: [
            'Aplicación / Plataforma Web'
        ],
        boton: 'Hablemos!'
    };

</script>

<div class="plans wrapper" id="scroll-plans">

    <div class="plans-info-top">
        <h2 id="scroll-planes">Planes</h2>
        <h4>Adquiere el mejor plan para tu sitio web</h4>
        <span>*No incluye costos de Hosting & Dominio</span>
        <br>
        <span>*No incluye IGV</span>
    </div>

    <div class="plans-cards">
        <div class="plans-card">
            <Card 
                {...basicPlan}
            />
        </div>

        <div class="plans-card">
            <Card 
                {...proPlan}
            />
        </div>

        <div class="plans-card">
            <Card 
                {...appPlan}
            />
        </div>
    </div>
</div>

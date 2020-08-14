<style>
    header{
        height: 100vh;
        width: 100%;
        position: relative;
        display: flex;
        background-image: url('/assets/header-bg.svg');
        background-size: cover;
    }
    .header-info{
        height: 100vh;
        position: relative;
        width: 100%;
    }

    .center-flex-row{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .header-about{
        width: 30%;
    }

    .header-title{
        margin-bottom: 10vh;
    }

    .header-message{
        margin-bottom: 8vh;
        max-width: 80%;
    }

    .networks{
        position: fixed;
        background-color: var(--primary);
        width: 100%;
        right: 0;
        bottom: 0;
        padding: 30px;
        margin-top: 100px;
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        align-items: center;
        z-index: 1;
    }

    .networks span{
        display: inline-block;
        margin-right: 20px;
        color: #fff;
    }


</style>

<script>

    import About from '../About/About.svelte';
    import BotonAction from '../Shared/BotonAction.svelte';
    import Networks from '../Shared/Networks.svelte';

</script>

<header>
    <div class="header-info shape center-flex">
        <div class="wrapper center-flex-row">
            <div class="content">
                <div class="header-title">
                    <h1 >Hola, Soy Nicolas</h1>
                    <h3 >Hagamos tu proyecto realidad!</h3>
                </div>
                <div class="header-message">
                    
                </div>
    
                <div class="header-action-buttons">
                    <BotonAction 
                        up={false} 
                        scroll={'#scroll-projects'}
                        text={'Proyectos'}/>
                    <BotonAction 
                        up={true} 
                        scroll={'#scroll-plans'}
                        text={'Ver planes'}/>
                </div>
            </div>

            <div class="header-about wrapper center-flex">
            </div>
        </div>

    </div>
        
    <div class="networks">
        <span>¿Necesitas una página web? Escríbeme</span>
        <Networks/>
    </div>

    

</header>
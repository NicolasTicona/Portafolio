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

    .header-content-center{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .header-title{
        margin-bottom: 10vh;
    }

    .header-networks{
        position: fixed;
        background-color: var(--primary);
        left: 0;
        bottom: 0;
        padding: 20px 30px;
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        align-items: center;
        border-radius: 0px 20px 20px 0;
        margin: 10px 10px 10px 0;
        z-index: 1;
    }

    .header-networks span{
        display: inline-block;
        margin-right: 20px;
        color: #fff;
    }

    .header-button{
        margin: 10px 0;
        display: inline-block;
    }
    
    @media screen and (max-width:768px){
        header{
            width: 100vw;
            background-color: var(--secondary);
            background-image: none;
        }

        .header-content{
            width: 100%;
            text-align: center;
        }

        .header-networks{
            padding: 20px;
        }
    }


</style>

<script>
    import BotonAction from '../Shared/BotonAction.svelte';
    import Networks from '../Shared/Networks.svelte';

</script>

<header class="header">
    <div class="header-info shape center-flex">
        <div class="wrapper header-content-center">
            <div class="header-content">
                <div class="header-title">
                    <h1 >Hola, Soy Nicolas</h1>
                    <h3 >Hagamos tu proyecto realidad!</h3>
                </div>
    
                <div class="header-action-buttons">
                    <div class="header-button">
                        <BotonAction 
                            up={false} 
                            scroll={'#scroll-projects'}
                            text={'Proyectos'}/>
                    </div>
                    <div class="header-button">
                        <BotonAction 
                            up={true} 
                            scroll={'#scroll-plans'}
                            text={'Trabajemos juntos'}/>
                    </div>
                </div>
            </div>

        </div>

    </div>
        
    <div class="header-networks">
        <span>Escríbeme, escucharé tu idea!</span>
        <Networks/>
    </div>

</header>
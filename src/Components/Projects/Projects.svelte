<style>

    .projects{
        text-align: center;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .projects-title{
        color: #fff;
    }

    .projects-card a{
        text-decoration: none;
        color: #fff;
        font-size: 20px;
        display: inline-block;
        background-color: var(--primary);
        padding: 20px 40px;
        border-radius: 10px;
        margin: 10px;
    }

    .projects-card:nth-child(odd){
        margin-left: 100px;
    }
    .projects-card:nth-child(even){
        margin-left: -100px;
    }

    .projects-link-github{
        color: #fff;
        margin-top: 20px;
        text-decoration: none;
        font-size: 13px;
    }

    @media screen and (max-width:768px){
        .projects-card a{
            font-size: 16px;
            padding: 15px 35px;
            margin: 8px;
        }
    }

</style>

<script>
    
</script>

<div class="projects" id="scroll-projects">
    <span class="projects-title">Proyectos con los que me formé</span>
    <div class="projects-card">
        <a class="shadow" href="https://smiledu.com">Colaboré en Smiledu</a>
    </div>
    <div class="projects-card">
        <a class="shadow" href="https://nicolasticona.github.io/Arkei">Arkei Chat</a>
    </div>
    <div class="projects-card">
        <a class="shadow" href="https://writerealtime.herokuapp.com/">WriteRealTime</a>
    </div>
    <div class="projects-card">
        <a class="shadow" href=".">PokeApi App</a>
    </div>
    <div class="projects-card">
        <a class="shadow" href=".">Clon Spotify</a>
    </div>

    <a class="projects-link-github" href=".">Más proyectos en <span>Github</span></a>
</div>
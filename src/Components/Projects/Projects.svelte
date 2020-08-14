<style>

    .projects{
        text-align: center;
    }

    .projects-container{
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
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

</style>

<script>
    
</script>

<div class="projects" id="scroll-projects">
    <div class="projects-container">
        <div class="projects-card">
            <a class="shadow" href=".">Smiledu</a>
        </div>
        <div class="projects-card">
            <a class="shadow" href=".">Arkei</a>
        </div>
        <div class="projects-card">
            <a class="shadow" href=".">WriteRealTime</a>
        </div>
        <div class="projects-card">
            <a class="shadow" href=".">Pokemon App</a>
        </div>
        <div class="projects-card">
            <a class="shadow" href=".">Spotify App</a>
        </div>

        <a class="projects-link-github" href=".">Más proyectos en <span>Github</span></a>
    </div>
</div>
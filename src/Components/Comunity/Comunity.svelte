<style>

    .comunity{
        width: 100%;
        background-color: var(--secondary);
        background-image: url('/assets/comunity-bg.svg');
        background-size: cover;
        background-position: center;
    }

    .comunity-youtube{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        flex-wrap: wrap;
        align-items: center;
        height: 60vh;
    }

    .comunity-youtube img{
        width: 40%;
        border-radius: 0 20px 20px 0;
    }

    .comunity-youtube h2{
        width: 50%;
        font-size: 50px;
        text-align: left;
    }

    @media screen and (max-width:768px){

        .comunity{
            background-image: none;
        }

        .comunity-youtube img{
            width: 80%;
        }

        .comunity-youtube h2{
            width: 90%;
            margin: auto;
            text-align: center;
            font-size: 30px !important;
        }
    
    }
    /* .plans-card:nth-child(2){
        margin-top: 50px;
    } */
</style>

<script>

</script>

<div class="comunity">
    <div class="comunity-youtube">
        <img src="/assets/youtube.JPG" class="shadow" alt="">
        <h2>
            ¡Únete a mi <a href="youhttps://www.youtube.com/channel/UC_3kEX4q9FNesZKuPKBMepw" target="_blank">comunidad</a> 
            y aprende conmigo!</h2>
    </div>
</div>

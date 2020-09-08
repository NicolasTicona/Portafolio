<style>

    .footer{
        background-color: var(--secondary);
        background-image: url('/assets/footer-pattern.png');
    }

    .footer-container{
        display: flex;
        flex-direction: row;
        align-items: center;
        flex-wrap: wrap;
        padding: 100px 0;
        padding-bottom: 40px;
    }

    .footer-section-left{
        width: 50%;
    }

    .footer-section-right{
        width: 50%;
        text-align: center;
    }

    .footer-credits{
        display: block;
        text-align: center;
        padding: 20px;
    }

    @media screen and (max-width:768px){
        .footer-section{
            width: 100%;
        }
    }


</style>

<script>
import Testimonial from '../Testimonial/Testimonial.svelte';
import Projects from '../Projects/Projects.svelte';

</script>

<div class="footer">
    <div class="footer-container wrapper">
        <div class="footer-section footer-section-left">
            <Testimonial />
        </div>

        <div class="footer-section footer-section-right">
            <Projects />
        </div>
    </div>

    <span class="footer-credits"><a href="/creditos.html" target="_blank">Créditos por íconos</a></span>
</div>


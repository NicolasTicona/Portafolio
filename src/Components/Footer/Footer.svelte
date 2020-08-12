<style>

    .footer{
        background-image: url('/assets/footer-pattern.png');
    }

    .footer-container{
        display: flex;
        flex-direction: row;
        align-items: center;
        padding: 100px 0;
    }

    .footer-section-left{
        width: 50%;
    }

    .footer-section-right{
        width: 50%;
        text-align: center;
    }



</style>

<script>
import Testimonial from '../Testimonial/Testimonial.svelte';
import Projects from '../Projects/Projects.svelte';

</script>

<div class="footer">
    <div class="footer-container wrapper">
        <div class="footer-section-left">
            <Testimonial />
        </div>

        <div class="footer-section-right">
            <Projects />
        </div>
    </div>
</div>


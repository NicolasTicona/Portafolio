<style>

/* General Styles */
:global(*){
	box-sizing: border-box !important;
	margin: 0;
	padding: 0;
}
:global(body){
	box-sizing: border-box;
	margin: 0;
	padding: 0;
	overflow-x: hidden;
	background-size: cover;
}

:global(h1){
	font-size: 70px;
}
:global(h2){
	font-size: 60px;
}
:global(h3){
	font-size: 30px;
}

:global(h4){
	font-size: 25px;
	font-weight: normal;
}

:global(p){
	font-size: 20px;
}

:global(.wrapper){
	padding: 20px;
}

:global(:root){
	--primary: #323232;
	--secondary: #f3f3f3;
}

:global(.center-flex){
	display: flex;
	flex-direction: column;
	justify-content: center;

	height: 100vh;
	width: 100%;
}

:global(hr){
	width: 40%;
	outline: none;
	margin: auto;
	border: 5px solid var(--primary);
}

:global(.shadow){
	box-shadow: 8px 8px 4px 0px rgba(0,0,0,0.25);
}

.container{
	position: absolute;
	top: 0;
	left: 0;
	width: 100vw;
}

@media screen and (max-width:768px){
		
	:global(h1){
		font-size: 50px !important;
	}
	:global(h2){
		font-size: 35px !important;
	}
	:global(h3){
		font-size: 20px !important;
	}

	:global(h4){
		font-size: 16px !important;
		font-weight: normal !important;
	}

	:global(p){
		font-size: 15px !important;
	}

	:global(span){
        display: inline-block;
		font-size: 13px !important;
	}
}


</style>

<script>


	import {showModal} from './Store/store.js';

	import Header from './Components/Header/Header.svelte';
	import About from './Components/About/About.svelte';
	import Plans from './Components/Plans/Plans.svelte';
	import Comunity from './Components/Comunity/Comunity.svelte';
	import Footer from './Components/Footer/Footer.svelte';	
	import Modal from './Components/Modal/Modal.svelte';

</script>
{#if $showModal}
	<div>
		<Modal />
	</div>
{/if}

<div class="container">
	<Header />

	<About />

	<Comunity />
	<Plans />


	<Footer />
</div>


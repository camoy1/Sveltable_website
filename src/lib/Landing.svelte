<script>
	import mainLogo from '../assets/main-logo.png';
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte'
	let show = false;
	onMount(()=>{
		show=!show
	})
</script>

{#if show}
<div class="landing-container" transition:fade="{{ delay: 500, duration: 2000 }}">
	<img src={mainLogo} alt="the svuture of data tables" />
	<div class="landing-text">the <b><i>sv</i></b>uture of data-tables is here</div>
	
	</div>
{/if}

<style>
	img {
		width: 60%;
	}

	.landing-container {
		display: flex;
    flex-direction: column;
		text-align: center;
		align-items: center;
		
	}

	.landing-text {
    padding-top: 1rem;
		font-family: 'IBM Plex Sans', sans-serif;
		color: white;
		font-size: 24px;
		font-weight: lighter;
	}
	
</style>

<script>
	import Img from '../assets/svelte_logo_resized.png';
</script>

<div class="landing-container">
	<img src={Img} alt="the svuture of data tables" />
	<div class="landing-text">the <b><i>sv</i></b>uture of datatables is here</div>
</div>

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

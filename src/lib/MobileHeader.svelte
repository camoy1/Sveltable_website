<script>
	import Hamburger from 'svelte-hamburgers';
	import MobileMenu from './MobileMenu.svelte';

	import mainLogo from '../assets/main-logo.png';

	let y = 0; // 'y' represents the user's y-axis scroll
	$: theme = y > 0 ? 'light' : 'dark'; // 'theme' represents light or dark background of header
	$: burgerTheme = y > 0 ? '#002940' : 'white';

	let open = false; // opening Hamburger component

	// function to trigger scrolling to different section/container
	const scrollTo = (containerName) => {
		document.querySelector(containerName).scrollIntoView({
			behavior: 'smooth'
		});
	};
</script>

<svelte:window bind:scrollY={y} />

<!-- Dictates dark/light theme for Mobile header row-->
<div class={`mobile-header-row-${theme}`}>
	<!-- Mobile header row container holding the full navigation bar -->
	<div class="mobile-header-row">
		<!-- Hamburger menu icon -->
		<Hamburger bind:open --color={`${burgerTheme}`} />
		<!-- <div>NEW</div> -->

		<!-- SvelTable logo icon -->
		<div class="menu-logo">
			<img id="logo-img" src={mainLogo} alt="svelte table logo" />
		</div>
	</div>
	<!-- MobileMenu opening -->
	<MobileMenu bind:open {theme} />
</div>

<style>
	.mobile-header-row {
		display: flex;
		justify-content: left;
		align-items: center;
		height: 3rem;
		transition: all 0.5s;
	}

	#logo-img {
		max-height: 2.5rem; /* sets img height to be slighter smaller than the header's height */
		padding: 0.2rem 0 0 1rem; /* centers logo vertically */
	}

	.mobile-header-row-dark {
		background-color: #002940;
		color: white;
		transition: all 0.5s;
	}

	.mobile-header-row-light {
		background-color: white;
		color: #002940;
		transition: all 0.5s;
	}
</style>

<script lang="ts">
	/**
	 * index.svelte is where we are rendering our site.
	 * Header.svelte is the header/navigation component.
	 * Landing.svelte is our landing page with our sveltable logo and description.
	 * Installation.svelte is the step-by-step guide with spritesheet for installation.
	 * Features.svelte is our text description of features within Sveltable.
	 * Demo.svelte is a component containing a gif of creating a table component and a description of it.
	 */
	import Team from '../lib/Team.svelte'
	import Header from '../lib/Header.svelte';
	import MobileHeader from '../lib/MobileHeader.svelte';
	import Landing from '../lib/Landing.svelte';
	import Installation from '../lib/Installation.svelte';
	import Demo from '../lib/Demo.svelte';
	import Features from '../lib/Features.svelte';
	let clientWidth;
</script>

<!-- Loading app -->
<div class="AppContainer" bind:clientWidth>
	<!-- Navigation Header -->
	<div class="HeaderContainer">
		{#if clientWidth > 800}
			<Header />
		{:else}
			<MobileHeader />
		{/if}
	</div>
	<!-- Landing body -->
	<div class="LandingContainer">
		<Landing />
	</div>
	<!-- Demo section -->
	{#if clientWidth > 800}
	<div class="DemoContainer">
		<Demo />
	</div>
	{/if}
	<!-- Installation section -->
	<div class="InstallationContainer">
		<Installation />
	</div>
	<!-- Features section -->
	<div class="FeatureContainer">
		<Features />
	</div>
	<div class="TeamContainer">
		<Team/>
	</div>
</div>

<style>
	.AppContainer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		/* background-color: #002940; */
	}

	.HeaderContainer {
		display: block;
		z-index: 1;
		width: 100vw;
		position: fixed;
		top: 0;
		left: 0;
	}

	.LandingContainer {
		display: flex;
		justify-content: center;
		align-items: center;
		min-height: 100vh;
	}

	.DemoContainer {
		min-height: 100vh;
	}

	.InstallationContainer {
		min-height: 100vh;
	}

	.FeatureContainer {
		min-height: 100vh;
	}
	.TeamContainer {
		min-height: 100vh;
	}
</style>

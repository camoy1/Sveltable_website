<script>
	import npmInstall from '../assets/npm-install.gif'
	import importPkg from '../assets/import-sveltable-demo.gif'
	import setupData from '../assets/data-setup-demo.gif'
	import setupRows from '../assets/numRows-demo.gif'
	let innerWidth;
	$: style = innerWidth > 1100 ? 'desktop' : 'mobile';
</script>

<svelte:window bind:innerWidth />

<div class={`SectionContainer-${style}`}>
	<div class="HeaderTitle">
		<h1>installation</h1>
	</div>

	<!-- Step 1: Install Container -->
	<div class={`StepContainer-left-${style}`}>
		<div class="Step">
			<p>
				<b>step 1:</b> install <strong><em>sveltable</em></strong> with
				<a href="https://www.npmjs.com/package/sveltable" target="_blank"> npm </a>
			</p>
		</div>
		<div class="GifContainer">
			<img src={npmInstall} alt="Demo of NPM install Terminal" />
		</div>
	</div>

	<!-- Step 2: Import Container -->
	<div class={`StepContainer-right-${style}`}>
		<div class="GifContainer">
			<img src={importPkg} alt="Demo of importing component" />
		</div>
		<div class="Step">
			<p>
				<b>step 2:</b> import <em>sveltable</em> into your application
			</p>
		</div>
	</div>

	<!-- Step 3: Data Setup Container -->
	<div class={`StepContainer-left-${style}`}>
		<div class="Step">
			<p>
				<b>step 3:</b> pass in your data
			</p>
		</div>
		<div class="GifContainer">
			<img src={setupData} alt="Demo of passing in data" />
		</div>
	</div>

	<!-- Step 4: Row Setup Container -->
	<div class={`StepContainer-right-${style}`}>
		<div class="GifContainer">
			<img src={setupRows} alt="Demo of setting up display row" />
		</div>
		<div class="Step">
			<p>
				<b>step 4:</b> specify how many rows to display
			</p>
		</div>
	</div>

</div>

<style>
	p {
		font-family: 'IBM Plex Sans', sans-serif;
	}

	.SectionContainer-desktop {
		padding: 4rem 0 4rem 0;
	}

	.SectionContainer-mobile {
		padding: 4rem 0 4rem 0;
	}

	.HeaderTitle {
		color: white;
		font-family: 'IBM Plex Sans', sans-serif;
		display: flex;
		justify-content: center;
	}

	.Step {
		margin: 0 1rem 0 1rem;
		color: white;
		font-family: 'IBM Plex Sans', sans-serif;
		font-weight: lighter;
		display: flex;
		font-size: 1.2rem;
	}

	.StepContainer-left-desktop,
	.StepContainer-right-desktop {
		margin: 0 2rem 0 2rem;
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-bottom: 50px;
	}

	.StepContainer-left-mobile {
		margin: 2rem 2rem 2rem 2rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.StepContainer-right-mobile {
		display: flex;
		flex-direction: column-reverse;
		align-items: center;
		justify-content: center;
	}

	.GifContainer {
		max-width: 80vw;
		padding: 0.5em 0.5em 0.5em 0.5em ;
		display: flex;
		align-items: center;
		justify-content: center;
		background-color: white;
	}
	.GifContainer img {
		max-height: 100%;
		max-width: 100%;
	}

	a:visited {
		color: white;
	}
</style>

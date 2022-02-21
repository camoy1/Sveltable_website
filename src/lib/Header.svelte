<script>
	import Img from '../assets/svelte_logo_resized.png';
	let y = 0; // 'y' represents the user's y-axis scroll
	$: theme = y > 0 ? 'light' : 'dark'; // 'theme' represents light or dark background of header

	// function to trigger scrolling to different section/container
	const scrollTo = (containerName) => {
		document.querySelector(containerName).scrollIntoView({
			behavior: 'smooth'
		});
	};
</script>

<svelte:window bind:scrollY={y} />

<div class={`header-${theme}`}>
	<div class="container-row">
		<!-- Left header navigation -->
		<div class={`menu-left ml-${theme}`}>
			<div class="head-btn" on:click={() => scrollTo('.DemoContainer')}>demo</div>
			<div class="head-btn" on:click={() => scrollTo('.FeatureContainer')}>features</div>
			<div class="head-btn" on:click={() => scrollTo('.TeamContainer')}>team</div>
		</div>

		<!-- Center header navigation -->
		<div class="menu-logo">
			<img id="logo-img" src={Img} alt="svelte table logo" />
		</div>

		<!-- Right header navigation -->
		<div class="menu-social">
			<a class="github-link" href="https://github.com/oslabs-beta/SvelTable" target="_blank">
				<div class={`git-${theme}`}>
					<i class="fab fa-github fa-2x" />
				</div>
			</a>
			<a class="linkedin-link" href="https://www.linkedin.com" target="_blank">
				<div class={`linkedin-${theme}`}>
					<i class={`fab fa-linkedin fa-2x`} />
				</div>
			</a>
			<a class="npm-link" href="https://www.npmjs.com/package/sveltable">
				<div class={`npm-${theme}`}>
					<i class="fab fa-npm fa-2x" />
				</div>
			</a>
		</div>
	</div>
</div>

<style>
	a {
		color: #e6e6e6;
	}

	.container-row {
		display: grid;
		height: 3rem;
		grid-template-columns: [left] 25vw [center] 50vw [right] 25vw;
		transition: all 0.5s;
	}

	.header-dark {
		background-color: #002940;
		color: #e6e6e6;
	}

	.header-light {
		background-color: #e6e6e6;
		color: #002940;
	}

	.menu-left {
		grid-area: left;
		display: flex;
		align-items: center;
		max-width: 25vw;
		font-family: 'IBM Plex Sans', sans-serif;
		border: 1px solid lightblue;
	}

	.menu-left div {
		margin-left: 0.5rem;
	}

	.menu-logo {
		grid-area: center;
		display: flex;
		justify-content: center;
		border: 1px solid red;
	}

	.menu-social {
		grid-area: right;
		display: flex;
		align-items: center;
		justify-content: flex-end;
		border: 1px solid white;
	}

	.menu-social a {
		margin-right: 0.5rem;
	}

	.git-light {
		color: #333; /* dark when header is light*/
	}

	.linkedin-light {
		color: #0077b5; /* linkedin blue directly from website when header is light */
	}

	.npm-light {
		color: #cc3534; /* red when header is light*/
	}

	.npm-dark {
		color: #e6e6e6; /* white when header is dark*/
	}

	.head-btn:hover,
	.menu-logo:hover,
	.item:hover {
		cursor: pointer; /* changes all hovering of buttons to be a pointer cursor */
	}

	#logo-img {
		max-height: 2.5rem; /* sets img height to be slighter smaller than the header's height */
	}

	@media screen and (max-width: 650px) {
	
	}
</style>

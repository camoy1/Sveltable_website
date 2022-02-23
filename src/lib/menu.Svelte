<script>
	import { fly } from 'svelte/transition';
	export let open = false;
	export let theme=undefined

	const scrollTo = (containerName) => {
		open=!open
		document.querySelector(containerName).scrollIntoView({
			behavior: 'smooth'
		});
	};
</script>

{#if open}
	<div class={`button mobile-text-${theme}`} transition:fly={{ y: -15, delay: 30 }} on:click={() => scrollTo('.InstallationContainer')}>installation</div>
	<div class={`button mobile-text-${theme}`} transition:fly={{ y: -15, delay: 30 *2}} on:click={() => scrollTo('.FeatureContainer')}>features</div>
	<div class={`button mobile-text-${theme}`} transition:fly={{ y: -15, delay: 30 *3}} on:click={() => scrollTo('.TeamContainer')}>team</div>
	<div class="mobile-icons" transition:fly={{ y: -15, delay: 30 *4}}>
		<a class="button npm-link" href="https://www.npmjs.com/package/sveltable" target="_blank">
			<div class={`npm-${theme}`}>
				<i class="fab fa-npm fa-2x" />
			</div>
		</a>
		<a class="button github-link" href="https://github.com/oslabs-beta/SvelTable" target="_blank">
			<div class={`git-${theme}`}>
				<i class="fab fa-github fa-2x" />
			</div>
		</a>
		<a class="button linkedin-link" href="https://www.linkedin.com/company/sveltable-open-source-product" target="_blank">
			<div class={`linkedin-${theme}`}>
				<i class={`fab fa-linkedin fa-2x`} />
			</div>
		</a>
	</div>
{/if}

<style>
	:global(html) {
		background: #002940;
	}
	.button {
		cursor: pointer;
	}
	
	div {
		align-items: right;
		font-size: 1rem;
		letter-spacing: 0.15em;
		padding: 1em;
		padding-top: 1em;
		color: white;
		font-family: 'IBM Plex Sans', sans-serif;
	}

	.mobile-icons {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-around;
	}

	.mobile-text-dark {
		color: white;
	}

	.mobile-text-light {
		color: #002940;
	}

	.npm-light {
		color: #cc3534; /* red when header is light*/
	}

	.npm-dark {
		color: white; /* white when header is dark*/
	}
	
	.git-light {
		color: #333; /* dark when header is light*/
	}

	.linkedin-light {
		color: #0077b5; /* linkedin blue directly from website when header is light */
	}
</style>

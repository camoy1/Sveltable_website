<script>
	import { fly, scale } from 'svelte/transition';
	import { quadOut } from 'svelte/easing';

	export let open = false;
</script>

{#if open}
	<div>
		{#each ['Tommy', 'Care', 'Boba', 'Milk'] as link, i}
			<p transition:fly={{ y: -15, delay: 50 * i }}>
				{link}
			</p>
		{/each}
	</div>
	<!-- <hr transition:scale={{ duration: 750, easing: quadOut, opacity: 1 }} /> -->
{/if}

<style>
	:global(html) {
		background: #002940;
	}

	div {
		/* align-items: right; */
		/* font-size: 2em; */
		/* letter-spacing: 0.15em; */
		/* padding: 1em; */
		/* padding-top: 0; */
		color: #e6e6e6;
	}

	p {
		cursor: pointer;
		width: max-content;
		/* margin: 1rem auto; */
	}

	p:hover {
		text-decoration: underline;
	}
</style>

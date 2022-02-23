<script>
	import columnSort from '../assets/column-sorting-demo.gif'
	import columnResize from '../assets/column-resizing-demo.gif'
	import multiFilter from '../assets/multifilter-demo.gif'
	import globalSearch from '../assets/search-bar-1-filter-demo.gif'
	let innerWidth;
	$: style = innerWidth > 1100 ? 'desktop' : 'mobile';
</script>

<svelte:window bind:innerWidth />

<div class={`SectionContainer-${style}`}>
	<div class="HeaderTitle">
		<h1>features</h1>
	</div>
	<!-- Global Search Container -->
	<div class={`StepContainer-left-${style}`}>
		<div class="Step">
			<p>
				<strong>search:</strong> search for values globally
			</p>
		</div>
		<div class="GifContainer">
			<img src={globalSearch} alt="Demo of global search feature" />
		</div>
	</div>

	<!-- Sort Container -->
	<div class={`StepContainer-right-${style}`}>
		<div class="GifContainer">
			<img src={columnSort} alt="Demo of importing component" />
		</div>
		<div class="Step">
			<p>
				<strong>sorting:</strong> sort any column
			</p>
		</div>
	</div>
	<!-- Multi Filter Container -->
	<div class={`StepContainer-left-${style}`}>
		<div class="Step">
			<p>
				<strong>multi-filter:</strong> filter multiple columns simultaneously
			</p>
		</div>
		<div class="GifContainer">
			<img src={multiFilter} alt="Demo of multiple filter" />
		</div>
	</div>

	<!-- Sort Container -->
	<div class={`StepContainer-right-${style}`}>
		<div class="GifContainer">
			<img src={columnResize} alt="Demo of resizing columns" />
		</div>
		<div class="Step">
			<p>
				<strong>resizing:</strong> resize any columns
			</p>
		</div>
	</div>
</div>

<style>
	.SectionContainer-desktop ,.SectionContainer-mobile{
		padding: 4rem 0 4rem 0;
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
		align-items: center;
		font-size: 1.2rem;
	}

	.GifContainer {
		max-width: 80vw;
		padding: 0.5em 0.5em 0.5em 0.5em ;
		display: flex;
		align-items: center;
		justify-content: center;
		background-color: #9c9c9c;
	}
	.GifContainer img {
		max-height: 100%;
		max-width: 100%;
	}
	
</style>

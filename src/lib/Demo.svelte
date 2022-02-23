<script>
	/**
	 * import namor for random data generation
	 */
	export let dataSet;
	import namor from 'namor';
	import SvelTable from 'sveltable';

	/**
	 * newPerson function
	 * @param num = number of rows to create
	 */
	
</script>

<div class="SectionContainer">
	<div class="HeaderTitle">
		<h1>demo</h1>
	</div>

	<div class="DemoContainer">
		<SvelTable dataSet={dataSet} />
	</div>
</div>

<style>
	.SectionContainer {
		padding: 4rem 0 4rem 0;
		justify-content: center;
	}

	.DemoContainer {
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.HeaderTitle {
		color: white;
		font-family: 'IBM Plex Sans', sans-serif;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 1.2rem;
	}
</style>

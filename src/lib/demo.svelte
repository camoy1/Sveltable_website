<script>
	/**
	 * import namor for random data generation
	 */
	import namor from 'namor';
	import SvelTable from 'sveltable';

	/**
	 * newPerson function
	 * @param num = number of rows to create
	 */
	function newPerson(num) {
		const sexAssigner = Math.random();
		return {
			id: num,
			firstName: namor.generate({ words: 1, numbers: 0 }),
			lastName: namor.generate({ words: 1, numbers: 0 }),
			sex: sexAssigner > 0.75 ? 'prefer not to say' : sexAssigner > 0.25 ? 'male' : 'female',
			age: Math.floor(Math.random() * 110),
			occupation: namor.generate({ words: 1, numbers: 0 })
		};
	}

	let userDefinedNum = 1000;

	let data = [];

	for (let i = 1; i < userDefinedNum + 1; i++) {
		let newP = newPerson(i);
		data.push(newP);
	}
</script>

<div class="SectionContainer">
	<div class="HeaderTitle">
		<h1>demo</h1>
	</div>

	<div class="DemoContainer">
		<SvelTable dataSet={data} />
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

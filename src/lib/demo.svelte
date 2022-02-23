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

	let userDefinedNum = 50;

	let data = [];

	for (let i = 1; i < userDefinedNum + 1; i++) {
		let newP = newPerson(i);
		data.push(newP);
	}
</script>

<div class="SectionContainer">
	<div class="HeaderTitle">
		<h2>demo</h2>
	</div>

	<div class="DemoContainer">
		<SvelTable dataSet={data} />
	</div>
</div>

<style>
	.SectionContainer {
		padding: 4rem 0 4rem 0;
	}

	.DemoContainer {
		padding-top: 2em;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.HeaderTitle {
		color: #fff;
		font-family: 'IBM Plex Sans', sans-serif;
		display: flex;
		justify-content: center;
	}
</style>

<script>
	export let name = "Bon";
	export let age = 27;

	$: uppercaseName = name.toUpperCase();

	$: console.log(name);

	$: if (name === "Bonnie") {
		age = 55;
	}
	
	const changeAge = () => {
		age++;
	};

	const changeName = () => {
		name = "Bonnie";
	};
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {uppercaseName}! {age}</h1>
<button on:click={changeAge}>Change Age</button>
<button on:click={changeName}>Change name</button>

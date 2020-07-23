<script>
	import Main from "./Main.svelte";

	let clicked = false;
	const handleCLick = () => clicked = !clicked;
</script>

<Main clicked={clicked} on:click={handleCLick} />

<style>
	body {
		margin: 0;
		padding: 0;
	}

</style>
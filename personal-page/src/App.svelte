<script>
	import Profile from "./components/Profile.svelte";
	import * as constant from './constants';
	import SideMenu from "./components/SideMenu.svelte";
	import ListOfSkills from "./menuComponents/ListOfSkills.svelte";

	let selectedItem = 0;
	const itemClickHandler = (id) => selectedItem = id;
</script>

<div class="container">
	<div class="left">

	</div>
	<div class="right">

	</div>
</div>

<style>
	body {
		margin: 0;
		padding: 0;
	}

	.container {
		height: 100%;
		display: flex;
		flex-direction: column;
		background: yellow;
		position: relative;
	}

	.left {
		top: 0;
		right: 0;
		position: absolute;

		border: 14rem solid transparent;
		border-top: 14rem solid crimson;
		border-right: 14rem solid crimson;

		transition: border-width 1s;
	}

	.left:hover {
		border-width: 16rem;
	}

	.right {
		position: absolute;
		bottom: 0;
		left: 0;

		border: 14rem solid transparent;
		border-bottom: 14rem solid darkmagenta;
		border-left: 14rem solid darkmagenta;

		transition: border-width 1s;
	}

	.right:hover {
		border-width: 16rem;
	}

</style>
<script>
	import Profile from "./components/Profile.svelte";
	import * as constant from './constants';
	import SideMenu from "./components/SideMenu.svelte";


	let selectedItem = 0;
	const itemClickHandler = (id) => selectedItem = id;
</script>

<div class="container">
	<div class="left">
		<Profile
				description={constant.profileDescription}
				name={constant.profileName}
				picUrl={constant.profilePic}
		/>
		<SideMenu
				selectedItem={selectedItem}
				itemClickHandler={itemClickHandler}
		/>
	</div>
	<div class="right">{constant.menuItems.find(el => el.id === selectedItem).label}</div>
</div>

<style>
	body {
		margin: 0;
		padding: 0;
	}

	.container {
		height: 100%;
		display: flex;
		flex-direction: row;
	}

	.left {
		flex: 1;
		border-right: 1px solid #000;
	}

	.right {
		padding: 10px;
		flex: 5;
	}
</style>
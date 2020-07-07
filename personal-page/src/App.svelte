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
	<div class="right">
		{#if selectedItem === 1}
			<ListOfSkills title={constant.education.title} items={constant.education.items}/>
			<ListOfSkills title={constant.experience.title} items={constant.experience.items}/>
			<ListOfSkills title={constant.interests.title} items={constant.interests.items}/>
		{/if}
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
		flex-direction: row;
	}

	.left {
		flex: 1;
		border-right: 1px solid #000;
	}

	.right {
		flex: 5;
	}
</style>
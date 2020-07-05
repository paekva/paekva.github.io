<script>
	import Profile from "./components/Profile.svelte";
	import * as constant from './constants';
</script>

<div class="container">
	<div class="left">
		<div class="profile">
			<Profile
					description={constant.profileDescription}
					name={constant.profileName}
					picUrl={constant.profilePic}
			/>
		</div>
	</div>
	<div class="right">right panel</div>
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
		padding: 10px;
		flex: 1;
		border-right: 1px solid #000;
	}

	.right {
		padding: 10px;
		flex: 6;
	}

	.profile{
		flex: 1;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
</style>
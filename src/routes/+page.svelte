<script lang="ts">
	import Player from '$lib/Player.svelte';

	import Fa from 'svelte-fa';
	import { faHouse, faMagnifyingGlass } from '@fortawesome/free-solid-svg-icons';
</script>

<div class="container">
	<div class="section home">
		<div class="link active">
			<Fa icon={faHouse} />
			<p>Home</p>
		</div>
		<div class="link">
			<Fa icon={faMagnifyingGlass} />
			<p>Search</p>
		</div>
	</div>
	<div class="section main">
		<h2>Good Evening</h2>
	</div>
	<div class="section library">
		<p>Your Library</p>
	</div>
	<div class="section player">
		<Player />
	</div>
</div>

<style lang="scss">
	@import 'src/variables';

	.container {
		display: grid;
		grid-template-columns: 1fr 3fr;
		grid-template-rows: 100px 1fr 75px;
		padding: 10px;
		width: calc(100% - 20px);
		height: calc(100vh - 20px);
		gap: 10px;
		font-size: 1.15rem;

		.section {
			border-radius: 15px;
		}
	}

	.home {
		padding: 20px;
		background-color: $background;
		display: flex;
		flex-direction: column;
		justify-content: center;
		gap: 20px;

		.link {
			display: flex;
			align-items: center;
			gap: 15px;
		}
	}

	.main {
		grid-column: 2 / 3;
		grid-row: 1 / 3;
		background-color: $background;
		padding: 20px;
	}

	.library {
		grid-row: 2 / 3;
		background-color: $background;
		padding: 20px;
	}

	.player {
		grid-column: 1 / 3;
		grid-row: 3 / 4;
	}
</style>

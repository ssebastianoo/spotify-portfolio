<script lang="ts">
	import Player from '$lib/Player.svelte';
	import PlaylistCard from '$lib/PlaylistCard.svelte';
	import Album from '$lib/assets/trench.jpg';

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
		<h2>Hey there, I'm Seb!</h2>
		<div class="list">
			<PlaylistCard title="Projects" cover={Album} />
			<PlaylistCard title="Social" cover={Album} />
			<PlaylistCard title="Skills" cover={Album} />
			<PlaylistCard title="Hobbies" cover={Album} />
		</div>
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
			cursor: pointer;

			&:not(.active) {
				opacity: 0.8;
				transition: opacity 0.2s ease-in-out;

				&:hover {
					opacity: 1;
				}
			}
		}
	}

	.main {
		grid-column: 2 / 3;
		grid-row: 1 / 3;
		background: linear-gradient(146deg, rgba(66, 32, 35, 1) -20%, rgba(18, 18, 18, 1) 100%);
		padding: 20px;

		.list {
			margin-top: 20px;
			display: flex;
			justify-content: space-between;
			flex-wrap: wrap;
			gap: 12px 0;
		}
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

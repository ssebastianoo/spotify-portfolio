<script lang="ts">
	import Player from '$lib/Player.svelte';
	import LibraryCard from '$lib/LibraryCard.svelte';
	import Blurryface from '$lib/assets/covers/blurryface.jpg';
	import TOP from '$lib/assets/covers/twenty_one_pilots.png';
	import Vessel from '$lib/assets/covers/vessel.jpg';
	import Trench from '$lib/assets/covers/trench.jpg';
	import seb from '$lib/assets/seb.png';
	import './styles.scss';
	import Fa from 'svelte-fa';
	import { faHouse, faMagnifyingGlass } from '@fortawesome/free-solid-svg-icons';
</script>

<div class="container">
	<div class="section home">
		<a class="link active" href="/">
			<Fa icon={faHouse} />
			<p>Home</p>
		</a>
		<a class="link" href="/">
			<Fa icon={faMagnifyingGlass} />
			<p>Search</p>
		</a>
	</div>
	<div class="section main">
		<header>
			<a href="/about">
				<img width="30" src={seb} alt="my avatar" />
			</a>
		</header>
		<slot />
	</div>
	<div class="section library">
		<p>Your Library</p>
		<div class="playlists">
			<LibraryCard title="Projects" artist="seb" cover={Blurryface} url="/projects" />
			<LibraryCard title="Social" artist="seb" cover={TOP} url="/social" />
			<LibraryCard title="Skills" artist="seb" cover={Vessel} url="/skills" />
			<LibraryCard title="Hobbies" artist="seb" cover={Trench} url="/hobbies" />
		</div>
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
			all: unset;
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
		position: relative;

		header {
			display: flex;
			justify-content: flex-end;
			z-index: 999;
			position: relative;
			height: 34px;
			align-items: center;

			a {
				display: flex;
			}

			img {
				border: 2px solid black;
				border-radius: 50%;
				transition: scale 0.1s ease-in-out;

				&:hover {
					scale: 1.1;
				}
			}
		}
	}

	.library {
		grid-row: 2 / 3;
		background-color: $background;
		padding: 10px;

		p {
			padding: 10px;
		}

		.playlists {
			display: flex;
			flex-direction: column;
		}
	}

	.player {
		grid-column: 1 / 3;
		grid-row: 3 / 4;
	}
</style>

<script lang="ts">
	import Album from '$lib/assets/trench.jpg';
	import TOP from '$lib/assets/twenty_one_pilots.jpg';

	import Fa from 'svelte-fa';
	import { faClock } from '@fortawesome/free-solid-svg-icons';
	import SongCard from '$lib/SongCard.svelte';
</script>

<div class="playlist">
	<div class="header">
		<div class="left">
			<img width="190" src={TOP} alt="Album cover" />
		</div>
		<div class="right">
			<p class="label">Playlist</p>
			<h1>Social</h1>
		</div>
	</div>
	<div class="songs">
		<div class="song labels">
			<div class="left">
				<div class="title">
					<p class="number">#</p>
					<p>Title</p>
				</div>
				<div class="album">
					<p>Album</p>
				</div>
			</div>
			<div class="right">
				<div />
				<Fa icon={faClock} />
			</div>
		</div>
		<SongCard
			number={1}
			title="Github"
			artist="github.com"
			album="ssebastianoo"
			cover={Album}
			url={'https://github.com/ssebastianoo'}
		/>
		<SongCard
			number={2}
			title="Twitter"
			artist="x.com"
			album="ssebastianoo"
			cover={Album}
			url={'https://twitter.com/ssebastianoo'}
		/>
	</div>
</div>

<style lang="scss">
	.songs {
		display: flex;
		flex-direction: column;
		margin-top: 20px;

		.labels {
			opacity: 0.5;
		}

		.song {
			all: unset;
			padding: 10px;
			display: flex;
			align-items: center;
			justify-content: space-between;
			font-weight: 400;
			font-size: 0.85em;

			.left {
				display: flex;
				width: calc(100% - 60px);
			}

			.right {
				display: flex;
				justify-content: space-between;
				width: 60px;
			}

			.title {
				display: flex;
				align-items: center;
				gap: 10px;
				width: 60%;
			}
		}
	}

	.header {
		display: flex;
		gap: 17px;

		.right {
			display: flex;
			flex-direction: column;
			justify-content: flex-end;

			.label {
				font-size: 0.8em;
			}

			h1 {
				font-size: 3em;
			}
		}
	}
</style>

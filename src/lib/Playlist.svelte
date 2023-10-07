<script lang="ts">
	import { faClock } from '@fortawesome/free-solid-svg-icons';
	import TOP from '$lib/assets/covers/twenty_one_pilots.png';
	import Fa from 'svelte-fa';

	export let title: string;
	export let cover: string;
</script>

<div class="playlist">
	<div class="header">
		<div class="left">
			<img height="190" src={cover} alt="Album cover" />
		</div>
		<div class="right">
			<p class="label">Playlist</p>
			<h1>{title}</h1>
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
		<slot />
	</div>
</div>

<style lang="scss">
	.songs {
		display: flex;
		flex-direction: column;
		margin-top: 20px;

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

		.labels {
			opacity: 0.6;
			border-bottom: 1px solid rgb(56, 56, 56);
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

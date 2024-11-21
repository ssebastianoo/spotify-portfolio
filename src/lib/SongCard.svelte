<script lang="ts">
	import Fa from 'svelte-fa';
	import { faHeart } from '@fortawesome/free-solid-svg-icons';

	interface Props {
		cover: string;
		title: string;
		artist: string;
		album: string;
		url: string;
		number: Number;
		rel?: boolean;
	}

	let {
		cover,
		title,
		artist,
		album,
		url,
		number,
		rel = false
	}: Props = $props();
</script>

<a class="song" href={url} target="_blank" rel={rel ? 'me' : ''}>
	<div class="left">
		<div class="title">
			<p class="number">{number}</p>
			<img src={cover} alt="song cover" width="45" />
			<div class="info">
				<p class="name">{title}</p>
				<p class="author">{artist}</p>
			</div>
		</div>
		<div class="album">
			<p>{album}</p>
		</div>
	</div>
	<div class="right">
		<div class="like">
			<Fa icon={faHeart} />
		</div>
		<div class="time">
			<p>4:56</p>
		</div>
	</div>
</a>

<style lang="scss">
	@import 'src/variables';

	.song {
		all: unset;
		padding: 10px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		font-weight: 400;
		font-size: 0.85em;
		border-radius: 5px;
		cursor: pointer;

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

			.info {
				display: flex;
				flex-direction: column;
				line-height: 18px;

				.name {
					font-weight: 600;
				}

				.author {
					opacity: 0.8;
				}
			}
		}

		.album {
			display: flex;
			align-items: center;
			gap: 10px;
			opacity: 0.8;
		}

		.number {
			width: 14px;
		}

		.like {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}

		.time {
			display: flex;
			align-items: center;
			justify-content: flex-end;
			opacity: 0.8;
		}

		&:hover {
			background-color: hsla(0, 0%, 100%, 0.058);
		}
	}

	@media (max-width: $mobileView) {
		.song {
			padding: 0;

			.album,
			.number {
				display: none;
			}

			.title {
				width: unset;
				gap: 12px;

				img {
					width: 50px;
				}
			}

			.right {
				width: unset;

				.time {
					display: none;
				}

				.like {
					font-size: 0.9em;
				}
			}

			&:hover {
				background-color: unset;
			}
		}
	}
</style>

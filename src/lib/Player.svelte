<script lang="ts">
	import Album from '$lib/assets/covers/trench.jpg';

	import Fa from 'svelte-fa';
	import {
		faShuffle,
		faBackwardStep,
		faPause,
		faForwardStep,
		faRepeat,
		faVolumeLow,
		faBars,
		faHeart
	} from '@fortawesome/free-solid-svg-icons';
</script>

<div class="player-container">
	<div class="info">
		<img src={Album} height="50" alt="Album cover" />
		<div class="text">
			<p class="title">Smithereens</p>
			<p class="artists">Twenty One Pilots</p>
		</div>
		<div class="heart">
			<Fa icon={faHeart} />
		</div>
	</div>
	<div class="player">
		<div class="controls">
			<div class="icon">
				<Fa icon={faShuffle} />
			</div>
			<div class="icon">
				<Fa icon={faBackwardStep} />
			</div>
			<div class="icon">
				<Fa icon={faPause} />
			</div>
			<div class="icon">
				<Fa icon={faForwardStep} />
			</div>
			<div class="icon">
				<Fa icon={faRepeat} />
			</div>
		</div>
		<div class="time">
			<span>0:58</span>
			<div class="line">
				<div />
			</div>
			<span>3:44</span>
		</div>
	</div>
	<div class="buttons">
		<div class="icon">
			<Fa icon={faBars} />
		</div>
		<div class="mobile-icons">
			<div class="icon">
				<Fa icon={faHeart} />
			</div>
			<div class="icon triangle" />
		</div>
		<div class="volume">
			<Fa icon={faVolumeLow} />
			<div class="line">
				<div />
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	@import 'src/variables';

	.player-container {
		user-select: none;
		display: flex;
		height: calc(100% - 20px);
		padding: 10px;
		justify-content: space-between;

		.icon {
			cursor: pointer;
			display: flex;
			align-items: center;
			justify-content: center;
		}
	}

	.info {
		display: flex;
		align-items: center;
		gap: 18px;

		img {
			border-radius: 2px;
		}

		.title {
			font-size: 0.9rem;
			cursor: pointer;

			&:hover {
				text-decoration: underline;
			}
		}

		.artists {
			font-size: 0.8rem;
			opacity: 0.6;
			margin-top: 5px;
			cursor: pointer;

			&:hover {
				text-decoration: underline;
			}
		}

		.heart {
			font-size: 0.9em;
			color: $accent;
			cursor: pointer;
		}
	}

	.player {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 5px;

		.controls {
			display: flex;
			gap: 22px;
			font-size: 1.2rem;
		}

		.time {
			display: flex;
			justify-content: space-between;
			align-items: center;
			gap: 10px;
			font-size: 0.8rem;

			.line {
				width: 200px;
			}
		}
	}

	.line {
		background-color: $variant;
		margin-top: 2px;
		height: 4px;
		border-radius: 50px;
		display: flex;
		align-items: center;

		div {
			width: 50%;
			height: 100%;
			background-color: white;
			border-radius: 50px;
		}
	}

	.buttons {
		display: flex;
		align-items: center;
		gap: 11px;

		.volume {
			display: flex;
			align-items: center;
			gap: 10px;

			.line {
				width: 100px;
			}
		}

		.mobile-icons {
			display: none;
			align-items: center;
			gap: 18px;

			.triangle {
				width: 0;
				height: 0;
				border-top: 8px solid transparent;
				border-bottom: 8px solid transparent;
				border-left: 13px solid white;
			}
		}
	}

	@media (max-width: $mobileView) {
		.player {
			display: none;
		}

		.player-container {
			background-color: rgb(26, 24, 24);
			border-radius: 10px;
		}

		.info {
			gap: 10px;

			img {
				height: 42px;
			}

			.heart {
				display: none;
			}
		}

		.buttons {
			gap: 18px;
			transform: translateX(-8px);

			.mobile-icons {
				display: flex;
			}

			.volume {
				display: none;
			}
		}
	}
</style>

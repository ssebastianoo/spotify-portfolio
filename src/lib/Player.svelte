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
		faBars
	} from '@fortawesome/free-solid-svg-icons';
</script>

<div class="player-container">
	<div class="info">
		<img src={Album} height="50" alt="Album cover" />
		<div class="text">
			<p class="title">Smithereens</p>
			<p class="artists">Twenty One Pilots</p>
		</div>
	</div>
	<div class="player">
		<div class="controls">
			<Fa icon={faShuffle} />
			<Fa icon={faBackwardStep} />
			<Fa icon={faPause} />
			<Fa icon={faForwardStep} />
			<Fa icon={faRepeat} />
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
		<Fa icon={faBars} />
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
		display: flex;
		height: calc(100% - 20px);
		padding: 10px;
		justify-content: space-between;
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
		}

		.artists {
			font-size: 0.8rem;
			opacity: 0.6;
			margin-top: 5px;
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
	}
</style>

<script lang="ts">
	import wallpaper from '$lib/assets/wallpaper.webp';
	import verified from '$lib/assets/icons/verified.webp';
	import Fa from 'svelte-fa';
	import { faShuffle } from '@fortawesome/free-solid-svg-icons';
</script>

<div class="about-container">
	<img src={wallpaper} alt="Wallpaper" class="wallpaper" height="250px" width="100%" />
	<div class="header">
		<div class="top">
			<div class="verified">
				<img src={verified} alt="Verified" width="16px" />
				<p>Verified Frontend Developer</p>
			</div>
			<h1>Sebastiano Girotto</h1>
		</div>
		<div class="bottom">
			<p class="listeners">69,420 monthly listeners</p>
		</div>
	</div>
	<div class="content">
		<div class="controls">
			<div class="play">
				<div class="triangle" />
			</div>
			<p class="following">Following</p>
		</div>
		<div class="mobile-controls">
			<div class="left">
				<p class="following">Following</p>
			</div>
			<div class="right">
				<div class="shuffle">
					<Fa icon={faShuffle} />
				</div>
				<div class="play">
					<div class="triangle" />
				</div>
			</div>
		</div>
		<div class="about">
			<p>
				I'm a Frontend developer from Venice, I love to design, developer and deploy silly web apps.
				I really enjoy tech, photography, music and graphic design, I'm currently studying
				multimedia arts in high school and I'm planning on getting a computer science degree. In my
				free time if I'm not coding I'm probably making music with FL Studio.
				<br /><br />
				My favorite and usual stuck is SvelteKit, TypeScript, SCSS and Postgres, but I'm open to any
				modern technology. I started way back in 2018 with Python to then move to JavaScript, ending
				in the Frontend world. More of me on my <a href="/social">social media</a>.
			</p>
		</div>
	</div>
</div>

<style lang="scss">
	@import 'src/variables';

	.wallpaper {
		object-fit: cover;
		position: absolute;
		object-position: center;
		top: 0;
		left: 0;
		filter: brightness(0.6);
		border-top-left-radius: 15px;
		border-top-right-radius: 15px;
	}

	.header {
		position: relative;
		height: 176px;
		padding-bottom: 20px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;

		.verified {
			display: flex;
			align-items: center;
			gap: 4px;

			p {
				font-size: 0.8em;
			}
		}

		h1 {
			font-size: 3.5em;
		}

		.listeners {
			font-size: 0.9em;
		}
	}

	.content {
		margin-top: 15px;
		font-size: 0.9em;
	}

	.controls {
		display: flex;
		align-items: center;
		gap: 20px;
		margin-bottom: 15px;

		.following {
			cursor: pointer;
			border-radius: 100px;
			border: 1px solid rgba(255, 255, 255, 0.288);
			padding: 5px 10px;
			font-size: 0.8em;
			transition: all 0.2s ease-in-out;

			&:hover {
				border-color: white;
				scale: 1.05;
			}
		}
	}

	.play {
		background-color: $accent;
		width: 40px;
		height: 40px;
		border-radius: 50%;
		display: flex;
		justify-content: center;
		align-items: center;
		cursor: pointer;
		transition: scale 0.2s ease-in-out;

		.triangle {
			width: 0;
			height: 0;
			border-top: 7px solid transparent;
			border-bottom: 7px solid transparent;
			border-left: 12px solid rgb(0, 0, 0);
			transform: translateX(1px);
		}

		&:hover {
			scale: 1.1;
		}
	}

	.mobile-controls {
		display: none;
		justify-content: space-between;
		align-items: center;
		margin-bottom: 25px;

		.right {
			display: flex;
			align-items: center;
			gap: 15px;
		}

		.following {
			padding: 6px 8px;
			border: 1px solid white;
			border-radius: 2px;
			font-size: 0.85em;
		}

		.shuffle {
			font-size: 1.35em;
		}

		.play {
			width: 45px;
			height: 45px;

			.triangle {
				border-top: 9px solid transparent;
				border-bottom: 9px solid transparent;
				border-left: 14px solid rgb(0, 0, 0);
				transform: translateX(2.2px);
			}
		}
	}

	.about {
		font-weight: 400;

		a {
			color: $accent;
		}
	}

	@media (max-width: $mobileView) {
		.header {
			padding-bottom: 0;
			height: 265px;
			justify-content: flex-end;
			gap: 21px;

			h1 {
				font-size: 2em;
			}
		}

		.wallpaper {
			top: -20px;
			left: -20px;
			border-radius: 0;
			width: calc(100% + 40px);
		}

		.controls {
			display: none;
		}

		.mobile-controls {
			display: flex;
		}

		.content {
			margin-top: 10px;
		}

		.about {
			height: calc(var(--fh) - 500px);
			overflow: auto;
		}
	}
</style>

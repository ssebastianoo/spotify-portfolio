<script lang="ts">
	import wallpaper from '$lib/assets/wallpaper.jpg';
	import verified from '$lib/assets/icons/verified.png';
</script>

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
	<div class="about">
		<p>
			I'm a Frontend developer from Venice, I'm not limited to JavaScript frameworks, I work with
			various technologies, from UI tools to Backend languages, from Adobe to Docker, any technology
			is welcome in my stack if it allows me to create new things.
			<br /><br />
			I'm currently studying multimedia arts in high school and I'm planning ot get a computer science
			degree.
			<br /><br />
			I really love rock and indie music,
		</p>
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
	}

	.about {
		font-weight: 400;
	}
</style>

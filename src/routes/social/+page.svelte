<script lang="ts">
	import Album from '$lib/assets/trench.jpg';

	const imageSize = 45;
</script>

<div class="playlist">
	<div class="header">
		<div class="left">
			<img width="190" src={Album} alt="Album cover" />
		</div>
		<div class="right">
			<p class="label">Playlist</p>
			<h1>Social</h1>
		</div>
	</div>
	<div class="songs">
		<div class="song">
			<div class="left">
				<p class="number">1</p>
				<img src={Album} alt="song cover" width={imageSize} />
				<div class="info">
					<p class="title">Twitter</p>
					<p class="author">x.com</p>
				</div>
			</div>
			<div class="right">
				<p class="album">ssebastianoo</p>
			</div>
		</div>
		<div class="song">
			<div class="left">
				<p class="number">1</p>
				<img src={Album} alt="song cover" width={imageSize} />
				<div class="info">
					<p class="title">Twitter</p>
					<p class="author">x.com</p>
				</div>
			</div>
			<div class="right">
				<p class="album">ssebastianoo</p>
			</div>
		</div>
		<div class="song">
			<div class="left">
				<p class="number">1</p>
				<img src={Album} alt="song cover" width={imageSize} />
				<div class="info">
					<p class="title">Twitter</p>
					<p class="author">x.com</p>
				</div>
			</div>
			<div class="right">
				<p class="album">ssebastianoo</p>
			</div>
		</div>
		<div class="song">
			<div class="left">
				<p class="number">1</p>
				<img src={Album} alt="song cover" width={imageSize} />
				<div class="info">
					<p class="title">Twitter</p>
					<p class="author">x.com</p>
				</div>
			</div>
			<div class="right">
				<p class="album">ssebastianoo</p>
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	.songs {
		display: flex;
		flex-direction: column;
		gap: 10px;
		margin-top: 20px;

		.song {
			display: flex;
			justify-content: space-between;
			align-items: centere;
			font-weight: 400;
			font-size: 0.85em;

			.left {
				display: flex;
				align-items: center;
				gap: 10px;

				.info {
					display: flex;
					flex-direction: column;
					line-height: 18px;

					.title {
						font-weight: 600;
					}

					.author {
						opacity: 0.8;
					}
				}
			}

			.right {
				display: flex;
				align-items: center;
				gap: 10px;

				.album {
					opacity: 0.8;
				}
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

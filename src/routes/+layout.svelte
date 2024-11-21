<script lang="ts">
	import Player from '$lib/Player.svelte';
	import LibraryCard from '$lib/LibraryCard.svelte';
	import Blurryface from '$lib/assets/covers/blurryface.webp';
	import TOP from '$lib/assets/covers/twenty_one_pilots.webp';
	import Vessel from '$lib/assets/covers/vessel.webp';
	import Trench from '$lib/assets/covers/trench.webp';
	import Clancy from '$lib/assets/covers/clancy.webp';
	import RAG from '$lib/assets/covers/rag.webp';
	import seb from '$lib/assets/seb.webp';

	import './styles.scss';
	import Fa from 'svelte-fa';
	import { faHouse, faMagnifyingGlass, faBarsStaggered } from '@fortawesome/free-solid-svg-icons';
	import { onMount } from 'svelte';

	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();

	onMount(() => {
		document.documentElement.style.setProperty('--fh', `${window.innerHeight}px`);
		window.addEventListener('resize', () => {
			document.documentElement.style.setProperty('--fh', `${window.innerHeight}px`);
		});
	});

	const children_render = $derived(children);
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
		{@render children_render?.()}
	</div>
	<div class="section library">
		<p>Your Library</p>
		<div class="playlists">
			<LibraryCard title="Projects" artist="seb" cover={Blurryface} url="/projects" />
			<LibraryCard title="Social" artist="seb" cover={TOP} url="/social" />
			<LibraryCard title="Skills" artist="seb" cover={Vessel} url="/skills" />
			<LibraryCard title="Hobbies" artist="seb" cover={Trench} url="/hobbies" />
			<LibraryCard title="About me" artist="seb" cover={Clancy} url="/about" />
			<LibraryCard title="Curriculum" artist="seb" cover={RAG} url="/CV.pdf" />
		</div>
	</div>
	<div class="section player">
		<Player />

		<footer>
			<a class="link" href="/">
				<Fa icon={faHouse} />
				<p>Home</p>
			</a>
			<a class="link" href="https://github.com/ssebastianoo/spotify-portfolio" target="_blank">
				<Fa icon={faMagnifyingGlass} />
				<p>Source code</p>
			</a>
			<a class="link" href="/about">
				<Fa icon={faBarsStaggered} />
				<p>Your Library</p>
			</a>
		</footer>
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
		height: calc(var(--fh) - 20px);
		gap: 10px;
		font-size: 1.15rem;
		position: relative;

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

	footer {
		display: none;
		justify-content: center;
		font-weight: 400;
		margin-top: 15px;

		.link {
			all: unset;
			display: flex;
			flex-direction: column;
			align-items: center;
			width: 33%;
			font-size: 0.85em;
			gap: 4px;
			cursor: pointer;

			p {
				font-size: 0.65em;
			}
		}
	}

	@media (max-width: $mobileView) {
		.container {
			display: block;
			font-size: 1.15rem;
			font-weight: 450;
			padding: 20px;
			width: calc(100% - 40px);
			height: calc(var(--fh) - 40px);

			.section {
				border-radius: unset;
			}
		}

		.library,
		.home {
			display: none;
		}

		.main {
			background: none;
			border-radius: unset;
			padding: 0;

			header {
				display: none;
			}
		}

		.player {
			position: absolute;
			width: calc(100% - 40px);
			bottom: 12px;
			left: 20px;
			border-radius: 10px !important;

			footer {
				display: flex;
			}
		}
	}
</style>

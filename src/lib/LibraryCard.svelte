<script lang="ts">
	import { onMount } from 'svelte';
	import { afterNavigate } from '$app/navigation';

	export let title: string;
	export let artist: string;
	export let cover: string;
	export let url: string;

	let active = false;

	function checkActive() {
		if (window.location.pathname === url) {
			active = true;
		} else {
			active = false;
		}
	}

	onMount(checkActive);
	afterNavigate(checkActive);
</script>

<a class="library-card" href={url} data-active={active}>
	<img src={cover} width="52" alt="Album cover" />
	<div class="text">
		<p class="title">{title}</p>
		<p class="artist">Playlist • {artist}</p>
	</div>
</a>

<style lang="scss">
	.library-card {
		all: unset;
		display: flex;
		align-items: center;
		gap: 10px;
		font-size: 0.9em;
		cursor: pointer;
		border-radius: 4px;
		padding: 10px;

		img {
			border-radius: 4px;
		}

		.artist {
			opacity: 0.7;
			font-weight: 400;
			font-size: 0.93em;
		}

		transition: background-color 0.2s ease-in-out;

		&:hover {
			background-color: hsla(0, 0%, 100%, 0.05);
		}

		&[data-active='true'] {
			background-color: hsla(0, 0%, 100%, 0.1);
		}
	}
</style>

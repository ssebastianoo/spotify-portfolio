<script lang="ts">
	interface Props {
		cover: string;
		title: string;
		url: string;
	}

	let { cover, title, url }: Props = $props();
</script>

<a class="card" href={url}>
	<img width="74" height="74" src={cover} alt="album cover" />
	<h3>{title}</h3>
</a>

<style lang="scss">
	@import 'src/variables';

	.card {
		all: unset;
		min-height: 74px;
		cursor: pointer;
		display: flex;
		align-items: center;
		gap: 15px;
		border-radius: 5px;
		background-color: hsla(0, 0%, 100%, 0.1);
		backdrop-filter: blur(10px);
		overflow: hidden;
		font-size: 0.8em;
		width: calc(33% - 5px);
		transition: background-color 0.2s ease-in-out;
		user-select: none;

		&:hover {
			background-color: hsla(0, 0%, 100%, 0.221);
		}
	}

	@media (max-width: 1200px) {
		.card {
			width: calc(50% - 5px);
		}
	}

	@media (max-width: 650px) {
		.card {
			width: calc(100% - 5px);
		}
	}
</style>

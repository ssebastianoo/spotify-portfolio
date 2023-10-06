<script lang="ts">
	export let cover: string;
	export let title: string;
	export let url: string;
</script>

<a class="card" href={url}>
	<img width="74" src={cover} alt="album cover" />
	<h3>{title}</h3>
</a>

<style lang="scss">
	@import 'src/variables';

	.card {
		all: unset;
		cursor: pointer;
		display: flex;
		align-items: center;
		gap: 15px;
		border-radius: 10px;
		background-color: hsla(0, 0%, 100%, 0.1);
		backdrop-filter: blur(10px);
		overflow: hidden;
		font-size: 0.8em;
		width: calc(33% - 5px);
		transition: background-color 0.2s ease-in-out;

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

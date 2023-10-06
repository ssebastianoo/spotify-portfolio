<script lang="ts">
	export let cover: string;
	export let title: string;
</script>

<div class="card">
	<img width="74" src={cover} alt="album cover" />
	<h3>{title}</h3>
</div>

<style lang="scss">
	@import 'src/variables';

	.card {
		display: flex;
		align-items: center;
		gap: 15px;
		border-radius: 10px;
		background-color: hsla(0, 0%, 100%, 0.1);
		backdrop-filter: blur(10px);
		overflow: hidden;
		font-size: 0.8em;
		width: calc(33% - 5px);
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

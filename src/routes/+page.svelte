<script lang="ts">
	import PlaylistCard from '$lib/PlaylistCard.svelte';
	import Album from '$lib/assets/trench.jpg';
</script>

<h2>Hey there, I'm Seb!</h2>
<div class="list">
	<PlaylistCard title="Projects" cover={Album} url={'/projects'} />
	<PlaylistCard title="Social" cover={Album} url={'/social'} />
	<PlaylistCard title="Skills" cover={Album} url={'/skills'} />
	<PlaylistCard title="Hobbies" cover={Album} url={'/hobbies'} />
</div>

<style lang="scss">
	.list {
		margin-top: 20px;
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		gap: 12px 0;
	}
</style>

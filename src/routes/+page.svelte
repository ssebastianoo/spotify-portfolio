<script lang="ts">
	import PlaylistCard from '$lib/PlaylistCard.svelte';

	import TOP from '$lib/assets/twenty_one_pilots.jpg';
	import Vessel from '$lib/assets/vessel.jpg';
	import Blurryface from '$lib/assets/blurryface.jpg';
	import Trench from '$lib/assets/trench.jpg';
</script>

<h2>Hey there, I'm Seb!</h2>
<div class="list">
	<PlaylistCard title="Projects" cover={Blurryface} url={'/projects'} />
	<PlaylistCard title="Social" cover={TOP} url={'/social'} />
	<PlaylistCard title="Skills" cover={Vessel} url={'#'} />
	<PlaylistCard title="Hobbies" cover={Trench} url={'#'} />
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

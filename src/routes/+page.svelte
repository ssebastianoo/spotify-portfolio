<script lang="ts">
	import PlaylistCard from '$lib/PlaylistCard.svelte';

	import TOP from '$lib/assets/covers/twenty_one_pilots.webp';
	import Vessel from '$lib/assets/covers/vessel.webp';
	import Blurryface from '$lib/assets/covers/blurryface.webp';
	import Trench from '$lib/assets/covers/trench.webp';
	import Clancy from '$lib/assets/covers/clancy.webp';
	import RAG from '$lib/assets/covers/rag.webp';
</script>

<h2>Hey there, I'm Seb!</h2>
<div class="list">
	<PlaylistCard title="Projects" cover={Blurryface} url="/projects" />
	<PlaylistCard title="Social" cover={TOP} url="/social" />
	<PlaylistCard title="Skills" cover={Vessel} url="/skills" />
	<PlaylistCard title="Hobbies" cover={Trench} url="/hobbies" />
	<PlaylistCard title="About me" cover={Clancy} url="/about" />
	<PlaylistCard title="Curriculum" cover={RAG} url="/CV.pdf" />
</div>

<style lang="scss">
	@import 'src/variables';

	.list {
		margin-top: 20px;
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		gap: 12px 0;
	}

	@media (max-width: $mobileView) {
		.list {
			flex-direction: column;
			height: calc(var(--fh) - 213px);
			flex-wrap: nowrap;
			overflow: auto;
			justify-content: unset;
		}
	}
</style>

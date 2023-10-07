<script lang="ts">
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import Trench from '$lib/assets/covers/trench.jpg';
	import missing from '$lib/assets/missing.png';
</script>

<Playlist title="Hobbies" cover={Trench}>
	<SongCard
		number={1}
		title="Photography"
		artist="📷"
		album="sony team"
		cover={missing}
		url={'https://unsplash.com/@ssebastianoo'}
	/>
	<SongCard
		number={2}
		title="Music Production"
		artist="soundcloud"
		album="fl studio kid"
		cover={missing}
		url={'https://soundcloud.com/sebps'}
	/>
</Playlist>

<script lang="ts">
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import Trench from '$lib/assets/covers/trench.webp';
	import banana from '$lib/assets/hobbies/banana.webp';
	import piano from '$lib/assets/hobbies/piano.webp';
</script>

<Playlist title="Hobbies" cover={Trench}>
	<SongCard
		number={1}
		title="Photography"
		artist="📷"
		album="sony team"
		cover={banana}
		url={'https://unsplash.com/@ssebastianoo'}
	/>
	<SongCard
		number={2}
		title="Music Production"
		artist="soundcloud"
		album="fl studio kid"
		cover={piano}
		url={'https://soundcloud.com/sebps'}
	/>
</Playlist>

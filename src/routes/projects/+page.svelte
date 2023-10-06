<script lang="ts">
	import Github from '$lib/assets/github.png';
	import Twitter from '$lib/assets/twitter.png';
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import Blurryface from '$lib/assets/blurryface.jpg';
	import GTE from '$lib/assets/gte.png';
	import FD from '$lib/assets/francescadiana.png';
</script>

<Playlist title={'Projects'} cover={Blurryface}>
	<SongCard
		number={1}
		title="Guess The Element"
		artist="gte.gir8.it"
		album="Svelte"
		cover={GTE}
		url={'https://gte.gir8.it'}
	/>
	<SongCard
		number={2}
		title="Francesca Diana"
		artist="francescadiana.pages.dev"
		album="HTML"
		cover={FD}
		url={'https://francescadiana.pages.dev/'}
	/>
</Playlist>

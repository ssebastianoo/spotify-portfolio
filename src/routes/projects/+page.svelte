<script lang="ts">
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import Blurryface from '$lib/assets/covers/blurryface.jpg';
	import GTE from '$lib/assets/projects/gte.png';
	import FD from '$lib/assets/projects/francescadiana.png';
	import missing from '$lib/assets/missing.png';
</script>

<Playlist title={'Projects'} cover={Blurryface}>
	<SongCard
		number={1}
		title="Portfolio"
		artist="gir8.it"
		album="HTML"
		cover={missing}
		url={'https://gir8.it'}
	/>
	<SongCard
		number={2}
		title="Guess The Element"
		artist="gte.gir8.it"
		album="Svelte"
		cover={GTE}
		url={'https://gte.gir8.it'}
	/>
	<SongCard
		number={3}
		title="Francesca Diana"
		artist="francescadiana.pages.dev"
		album="HTML"
		cover={FD}
		url={'https://francescadiana.pages.dev/'}
	/>
	<SongCard
		number={4}
		title="PlajHome"
		artist="plajhome.com"
		album="Astro"
		cover={missing}
		url={'https://plajhome.com'}
	/>
	<SongCard
		number={4}
		title="idle"
		artist="idle.gir8.it"
		album="Svelte"
		cover={missing}
		url={'https://idle.gir8.it'}
	/>
</Playlist>

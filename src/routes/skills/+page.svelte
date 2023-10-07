<script lang="ts">
	import Github from '$lib/assets/social/github.png';
	import Twitter from '$lib/assets/social/twitter.png';
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import Vessel from '$lib/assets/covers/vessel.jpg';
	import missing from '$lib/assets/missing.png';
</script>

<Playlist title="Skills" cover={Vessel}>
	<SongCard
		number={1}
		title="HTML / CSS"
		artist="not a programming language"
		album="3+ years"
		cover={missing}
		url={'https://it.wikipedia.org/wiki/HTML'}
	/>
	<SongCard
		number={2}
		title="JavaScript"
		artist="only one thread???"
		album="3+ years"
		cover={missing}
		url={'https://developer.mozilla.org/en-US/docs/Web/JavaScript'}
	/>
	<SongCard
		number={3}
		title="TypeScript"
		artist="love and hate"
		album="1+ year"
		cover={missing}
		url={'https://www.typescriptlang.org/'}
	/>
	<SongCard
		number={3}
		title="Python"
		artist="where it all started"
		album="3+ years"
		cover={missing}
		url={'https://www.python.org/'}
	/>
</Playlist>

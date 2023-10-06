<script lang="ts">
	import Github from '$lib/assets/github.png';
	import Twitter from '$lib/assets/twitter.png';
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import TOP from '$lib/assets/twenty_one_pilots.jpg';
</script>

<Playlist title={'Social'} cover={TOP}>
	<SongCard
		number={1}
		title="Github"
		artist="github.com"
		album="ssebastianoo"
		cover={Github}
		url={'https://github.com/ssebastianoo'}
	/>
	<SongCard
		number={2}
		title="Twitter"
		artist="x.com"
		album="ssebastianoo"
		cover={Twitter}
		url={'https://twitter.com/ssebastianoo'}
	/>
</Playlist>

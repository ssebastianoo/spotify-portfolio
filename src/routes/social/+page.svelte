<script lang="ts">
	import Github from '$lib/assets/social/github.png';
	import Twitter from '$lib/assets/social/twitter.png';
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import TOP from '$lib/assets/covers/twenty_one_pilots.png';
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

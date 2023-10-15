<script lang="ts">
	import TOP from '$lib/assets/covers/twenty_one_pilots.webp';
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import Github from '$lib/assets/social/github.webp';
	import Mastodon from '$lib/assets/social/mastodon.webp';
	import Twitter from '$lib/assets/social/twitter.webp';
	import Linkedin from '$lib/assets/social/linkedin.webp';
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
		title="Mastodon"
		artist="fosstodon.org"
		album="ssebastianoo"
		cover={Mastodon}
		rel={true}
		url={'https://fosstodon.org/@ssebastianoo'}
	/>
	<SongCard
		number={3}
		title="Twitter"
		artist="x.com"
		album="ssebastianoo"
		cover={Twitter}
		url={'https://twitter.com/ssebastianoo'}
	/>
	<SongCard
		number={4}
		title="Linkedin"
		artist="linkedin.com"
		album="sebastianogirotto"
		cover={Linkedin}
		url={'https://linkedin.com/in/sebastianogirotto'}
	/>
</Playlist>

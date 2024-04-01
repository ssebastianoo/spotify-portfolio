<script lang="ts">
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import Blurryface from '$lib/assets/covers/blurryface.webp';
	import GTE from '$lib/assets/projects/gte.webp';
	import FD from '$lib/assets/projects/francescadiana.webp';
	import portofolio from '$lib/assets/projects/portfolio.webp';
	import plajhome from '$lib/assets/projects/plajhome.webp';
	import idle from '$lib/assets/projects/idle.webp';
	import wheel from '$lib/assets/projects/wheel.webp';
	import fabiopizzano from '$lib/assets/projects/fabiopizzano.webp';
	import fastdaw from '$lib/assets/projects/fastdaw.webp';
	import ytdlp from '$lib/assets/projects/ytdlp.webp';
	import cronus from '$lib/assets/projects/cronus.webp';
</script>

<Playlist title={'Projects'} cover={Blurryface}>
	<SongCard
		number={1}
		title="Cronus"
		artist="cronus.lol"
		album="Next.js"
		cover={cronus}
		url={'https://cronus.lol'}
	/>
	<SongCard
		number={2}
		title="Old portfolio"
		artist="old.gir8.it"
		album="HTML + SCSS"
		cover={portofolio}
		url={'https://old.gir8.it'}
	/>
	<SongCard
		number={3}
		title="Guess The Element"
		artist="gte.gir8.it"
		album="Svelte"
		cover={GTE}
		url={'https://gte.gir8.it'}
	/>
	<SongCard
		number={4}
		title="Francesca Diana"
		artist="francescadiana.pages.dev"
		album="HTML + SCSS"
		cover={FD}
		url={'https://francescadiana.pages.dev/'}
	/>
	<SongCard
		number={5}
		title="Fabio Pizzano"
		artist="fabiopizzano.com"
		album="HTML + SCSS"
		cover={fabiopizzano}
		url={'http://fabiopizzano.com/'}
	/>
	<SongCard
		number={6}
		title="PlajHome"
		artist="plajhome.com"
		album="Astro"
		cover={plajhome}
		url={'https://plajhome.com'}
	/>
	<SongCard
		number={7}
		title="idle"
		artist="idle.gir8.it"
		album="Svelte"
		cover={idle}
		url={'https://idle.gir8.it'}
	/>
	<SongCard
		number={8}
		title="Wheel"
		artist="wheel.gir8.it"
		album="Svelte + TS"
		cover={wheel}
		url={'https://wheel.gir8.it'}
	/>
	<SongCard
		number={9}
		title="FastDaw"
		artist="fastdaw.vercel.app"
		album="Svelte + TS"
		cover={fastdaw}
		url={'https://fastdaw.vercel.app/'}
	/>
	<SongCard
		number={10}
		title="YT-DLP Telegram"
		artist="github.com"
		album="Svelte + TS"
		cover={ytdlp}
		url={'https://github.com/ssebastianoo/yt-dlp-telegram'}
	/>
</Playlist>

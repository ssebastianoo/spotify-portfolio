<script lang="ts">
	import Playlist from '$lib/Playlist.svelte';
	import SongCard from '$lib/SongCard.svelte';
	import Vessel from '$lib/assets/covers/vessel.webp';
	import html from '$lib/assets/skills/html.webp';
	import javascript from '$lib/assets/skills/javascript.webp';
	import typescript from '$lib/assets/skills/typescript.webp';
	import figma from '$lib/assets/skills/figma.webp';
	import python from '$lib/assets/skills/python.webp';
	import svelte from '$lib/assets/skills/svelte.webp';
	import react from '$lib/assets/skills/react.webp';
	import astro from '$lib/assets/skills/astro.webp';
	import scss from '$lib/assets/skills/scss.webp';
	import linux from '$lib/assets/skills/linux.webp';
	import nginx from '$lib/assets/skills/nginx.webp';
	import postgres from '$lib/assets/skills/postgres.webp';
	import firebase from '$lib/assets/skills/firebase.webp';
	import git from '$lib/assets/skills/git.webp';
	import docker from '$lib/assets/skills/docker.webp';
	import illustrator from '$lib/assets/skills/illustrator.webp';
	import photoshop from '$lib/assets/skills/photoshop.webp';
	import premiere from '$lib/assets/skills/premiere.webp';
	import tailwind from '$lib/assets/skills/tailwind.webp';
	import shadcn from '$lib/assets/skills/shadcn.webp';
	import caddy from '$lib/assets/skills/caddy.webp';
	import supabase from '$lib/assets/skills/supabase.webp';
</script>

<Playlist title="Skills" cover={Vessel}>
	<SongCard
		number={1}
		title="HTML / CSS"
		artist="not a programming language"
		album="3+ years"
		cover={html}
		url={'https://it.wikipedia.org/wiki/HTML'}
	/>
	<SongCard
		number={2}
		title="JavaScript"
		artist="only one thread???"
		album="3+ years"
		cover={javascript}
		url={'https://developer.mozilla.org/en-US/docs/Web/JavaScript'}
	/>
	<SongCard
		number={3}
		title="TypeScript"
		artist="love and hate"
		album="1+ year"
		cover={typescript}
		url={'https://www.typescriptlang.org/'}
	/>
	<SongCard
		number={4}
		title="Figma"
		artist="love love love"
		album="1+ years"
		cover={figma}
		url={'https://www.figma.com/'}
	/>
	<SongCard
		number={5}
		title="Python"
		artist="where it all started"
		album="4+ years"
		cover={python}
		url={'https://www.python.org/'}
	/>
	<SongCard
		number={6}
		title="Svelte"
		artist="my beloved"
		album="2+ years"
		cover={svelte}
		url={'https://svelte.dev/'}
	/>
	<SongCard
		number={7}
		title="React"
		artist="facebook kid"
		album="2+ years"
		cover={react}
		url={'https://reactjs.org/'}
	/>
	<SongCard
		number={8}
		title="Astro"
		artist="svelte + react"
		album="1+ year"
		cover={astro}
		url={'https://astro.build/'}
	/>
	<SongCard
		number={9}
		title="Tailwind"
		artist="css was boring"
		album="1+ year"
		cover={tailwind}
		url={'https://tailwindcss.com/'}
	/>
	<SongCard
		number={10}
		title="shadcn/ui"
		artist="it just works"
		album="months"
		cover={shadcn}
		url={'https://ui.shadcn.com/'}
	/>
	<SongCard
		number={11}
		title="SCSS"
		artist="never without it"
		album="3+ years"
		cover={scss}
		url={'https://sass-lang.com/'}
	/>
	<SongCard
		number={12}
		title="Linux"
		artist="raspberrypi nerd"
		album="3+ years"
		cover={linux}
		url={'https://en.wikipedia.org/wiki/Linux'}
	/>
	<SongCard
		number={13}
		title="Nginx"
		artist="ip shield"
		album="3+ years"
		cover={nginx}
		url={'https://www.nginx.com/'}
	/>
	<SongCard
		number={14}
		title="Caddy"
		artist="better nginx"
		album="months"
		cover={caddy}
		url={'https://caddyserver.com/'}
	/>
	<SongCard
		number={15}
		title="PostgreSQL"
		artist="best db"
		album="2+ years"
		cover={postgres}
		url={'https://www.postgresql.org/'}
	/>
	<SongCard
		number={16}
		title="Supabase"
		artist="better firebase"
		album="2+ years"
		cover={supabase}
		url={'https://supabase.com/'}
	/>
	<SongCard
		number={17}
		title="Firebase"
		artist="google kid"
		album="2+ years"
		cover={firebase}
		url={'https://firebase.google.com/'}
	/>
	<SongCard
		number={18}
		title="Git"
		artist="git gud"
		album="4+ years"
		cover={git}
		url={'https://git-scm.com/'}
	/>
	<SongCard
		number={19}
		title="Docker"
		artist="my greatest fear"
		album="1+ year"
		cover={docker}
		url={'https://www.docker.com/'}
	/>
	<SongCard
		number={20}
		title="Illustrator"
		artist="vectorrrr"
		album="5+ years"
		cover={illustrator}
		url={'https://www.adobe.com/products/illustrator.html'}
	/>
	<SongCard
		number={21}
		title="Photoshop"
		artist="pixellll"
		album="6+ years"
		cover={photoshop}
		url={'https://www.adobe.com/products/photoshop.html'}
	/>
	<SongCard
		number={22}
		title="Premiere"
		artist="I like moviess"
		album="5+ years"
		cover={premiere}
		url={'https://www.adobe.com/products/premiere.html'}
	/>
</Playlist>

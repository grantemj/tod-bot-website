<script>
	import MediaQuery from 'svelte-media-query'
	import DesktopNavbar from './DesktopNavbar.svelte'
	import DesktopNavbarCompact from './DesktopNavbarCompact.svelte'
	import MobileNavbar from './MobileNavbar.svelte'
	import Info from './Info.svelte'
	import About from './About.svelte'
</script>

<main>
	<MediaQuery query="(min-width: 811px)" let:matches>
		{#if matches}
			<MediaQuery query="(min-width: 1181px)" let:matches>
				{#if matches}
					<DesktopNavbar />
				{:else}
					<DesktopNavbarCompact />
				{/if}
			</MediaQuery>
		{:else}
			<MobileNavbar />
		{/if}
	</MediaQuery>
	<body>
		<Info serverCount=61576/>
		<About />
	</body>
</main>

<style>
	body {
		margin: 0;
		background: #2d2d2f;
		color: #f4f1eb;
	}
</style>
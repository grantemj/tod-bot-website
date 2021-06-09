<script>
	import DesktopNavbar from './DesktopNavbar.svelte'
	import DesktopNavbarCompact from './DesktopNavbarCompact.svelte'
	import MobileNavbar from './MobileNavbar.svelte'
	import Info from './Info.svelte'
	import About from './About.svelte'
	import GetStarted from './GetStarted.svelte'
	import Commands from './Commands.svelte'
	import Contact from './Contact.svelte'

	(async function() {
		let response = await fetch('https://truthordarebot.xyz/server_count')
		serverCount = await response.text()
	})()
	var serverCount = 0

	let viewingWidth = 1440
	$: viewingMode = (viewingWidth < 841) ? 'mobile' : (viewingWidth < 1181) ? 'compact' : 'desktop'

	$: { 	// text divs
		let calculatedWidth = (720 / viewingWidth) - 0.1; 	// width of text div in decimal relative to the page
		([...(document.getElementsByClassName("text"))]).forEach(item => {
			item.style.width = Math.max(40, Math.min(calculatedWidth * 100, 80)) + "%"
		})
	}

	$: {	// row (in commands section)
		let calculatedWidth = (1/13) + (997 / viewingWidth);  // width of row in decimal with respect to the page
		([...document.getElementsByClassName("row")]).forEach(item => {
			item.style.width = Math.max(70, Math.min(calculatedWidth * 100, 95)) + "%"
		})
	}

	$: { 	// tooltips
		let columnWidth = document.querySelector(".column")?.clientWidth || viewingWidth / 3
		// ^ width of column in px
		let calculatedWidth = 237.5 + 138.7 / (1 + Math.exp((columnWidth / -54) + 8.81));
		([...document.getElementsByClassName("tooltip")]).forEach(item => {
			item.style.width = calculatedWidth + "px"
		})
	}
</script>

<svelte:window bind:innerWidth={viewingWidth}/>

<main>
	{#if viewingMode === 'mobile'}
		<MobileNavbar />
	{:else if viewingMode === 'compact'}
		<DesktopNavbarCompact />
	{:else if viewingMode === 'desktop'}
		<DesktopNavbar />
	{/if}
	<body>
		<Info serverCount={serverCount} viewingMode={viewingMode}/>
		<About />
		<GetStarted />
		<Commands viewingMode={viewingMode} />
		<Contact />
	</body>
</main>

<style>
	body {
		margin: 0;
		background: #2d2d2f;
		color: #f4f1eb;
	}
</style>
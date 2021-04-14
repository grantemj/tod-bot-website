<script>
	import DesktopNavbar from './DesktopNavbar.svelte'
	import DesktopNavbarCompact from './DesktopNavbarCompact.svelte'
	import MobileNavbar from './MobileNavbar.svelte'
	import Info from './Info.svelte'
	import About from './About.svelte'
	import GetStarted from './GetStarted.svelte'
	import Commands from './Commands.svelte'
	import Contact from './Contact.svelte'

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
		let columnWidth = Math.max(70, Math.min((100/13) + (99700 / viewingWidth), 100)) * viewingWidth / 3
		// ^ width of column in px
		let calculatedWidth = 250 + 146 / (1 + Math.exp((viewingWidth / -153) + 8.37));
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
		<Info serverCount=61576 viewingMode={viewingMode}/>
		<About />
		<GetStarted />
		<Commands />
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
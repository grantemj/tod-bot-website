<script>
	import DesktopNavbar from './DesktopNavbar.svelte'
	import DesktopNavbarCompact from './DesktopNavbarCompact.svelte'
	import MobileNavbar from './MobileNavbar.svelte'
	import Info from './Info.svelte'
	import About from './About.svelte'
	import GetStarted from './GetStarted.svelte'
	import Commands from './Commands.svelte'

	let viewingWidth = 1440
	$: viewingMode = (viewingWidth < 841) ? 'mobile' : (viewingWidth < 1181) ? 'compact' : 'desktop'

	function resizeText() {
		let currentWidth = window.innerWidth
		let calculatedWidth = (720 / currentWidth) - 0.1;
		([...(document.getElementsByClassName("text"))]).forEach(item => {
			item.style.width = Math.max(40, Math.min(calculatedWidth * 100, 80)) + "%"
		})
	}

	function resizeRows() {
		let currentWidth = window.innerWidth
		let calculatedWidth = (1/13) + (997 / currentWidth);
		([...document.getElementsByClassName("row")]).forEach(item => {
			item.style.width = Math.max(70, Math.min(calculatedWidth * 100, 100)) + "%"
		})
	}

	window.onload = () => {
		resizeText()
		resizeRows()
	}
</script>

<svelte:window bind:innerWidth={viewingWidth} on:resize={() => {resizeText(); resizeRows();}}/>

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
	</body>
</main>

<style>
	body {
		margin: 0;
		background: #2d2d2f;
		color: #f4f1eb;
	}
</style>
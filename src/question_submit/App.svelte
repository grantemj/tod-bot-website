<script>
    import DesktopNavbar from '../DesktopNavbar.svelte'
	import DesktopNavbarCompact from '../DesktopNavbarCompact.svelte'
	import MobileNavbar from '../MobileNavbar.svelte'
    
    let viewingWidth = 1440
	$: viewingMode = (viewingWidth < 841) ? 'mobile' : (viewingWidth < 1181) ? 'compact' : 'desktop'

    $: {
        let calculatedWidth = (720 / viewingWidth) - 0.1; 	// width of form in decimal relative to the page
		let item = document.getElementById("form")
		item.style.width = Math.max(40, Math.min(calculatedWidth * 100, 80)) + "%"
    }
</script>

<svelte:window bind:innerWidth={viewingWidth} />

<main>
    {#if viewingMode === 'mobile'}
		<MobileNavbar />
	{:else if viewingMode === 'compact'}
		<DesktopNavbarCompact />
	{:else if viewingMode === 'desktop'}
		<DesktopNavbar />
	{/if}
    <body>
        <h1>Question Submission Form</h1>

    </body>
</main>

<style>
    body {
		margin: 0;
		background: #2d2d2f;
		color: #f4f1eb;
	}
</style>
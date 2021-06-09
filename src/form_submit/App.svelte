<script>
    import DesktopNavbar from '../DesktopNavbar.svelte'
	import DesktopNavbarCompact from '../DesktopNavbarCompact.svelte'
	import MobileNavbar from '../MobileNavbar.svelte'
    
    let viewingWidth = 1440
	$: viewingMode = (viewingWidth < 841) ? 'mobile' : (viewingWidth < 1181) ? 'compact' : 'desktop'

    $: {
        let calculatedWidth = (720 / viewingWidth) - 0.1; 	// width of form in decimal relative to the page
		let item = document.getElementById("form")
		if (item) item.style.width = Math.max(40, Math.min(calculatedWidth * 100, 80)) + "%"
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
        <h1 class="section-title">Form Submitted Successfully</h1>
		<a href="/" target="_self"><button type="button">Home</button></a><br>
        <a href="/feedback"><button type="button">Give Feedback</button></a><br>
        <a href="/question_submit"><button type="button">Submit Questions</button></a><br>
    </body>
</main>

<style>
    body {
		margin: 0;
		padding-top: 160px;
		padding-bottom: 160px;
		background: #2d2d2f;
		color: #f4f1eb;
		text-align: center;
		min-height: 100vh;
	}

    a * {
        border: solid 3px #2d3966;
        border-radius: 9px;
    }

    button {
        background: #202122;
        color: #f4f1eb;
        font-family: "Rubik";
        font-size: 1.25rem;
        cursor: pointer;
        padding: 0.4em;
        margin: 0.5em 0;
    }
</style>
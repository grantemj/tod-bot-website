<script>
    export let serverCount
    export let viewingMode
</script>

<div id="info">
    <img src="https://truthordarebot.xyz/PFP.png" alt="Profile pic" id="main-pfp" class={viewingMode}>
    <h2>Currently in <code>{serverCount}</code> servers</h2>
</div>

<style>
    #info {
        width: 100%;
        text-align: center;
        padding-top: 14rem;
        padding-bottom: 4.375rem;
    }

    #main-pfp {
        border-radius: 50%;
    }

    code {
        font-size: 2.5rem;
        color: inherit;
        background: none;
        padding: 0;
        text-decoration: underline;
    }

    h2 {
        font-size: 2.25rem;
        font-weight: 600;
        color: #cd8a3f;
    }

    img.desktop {
        width: 22rem;
        height: 22rem;
    }

    img.compact {
        width: 18rem;
        height: 18rem;
    }

    img.mobile {
        width: 14rem;
        height: 14rem;
    }
</style>
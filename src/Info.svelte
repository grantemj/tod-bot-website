<script>
    export let serverCount
</script>

<main>
    <img src="https://truthordarebot.xyz/PFP.png" alt="Profile pic" id="main-pfp">
    <h2>Currently in <code>{serverCount}</code> servers</h2>
</main>

<style>
    main {
        width: 100%;
        text-align: center;
    }

    #main-pfp {
        border-radius: 50%;
        width: 450px;
        height: 450px;
    }

    code {
        font-size: 40px;
        color: inherit;
        background: none;
        padding: 0;
        text-decoration: underline;
    }

    h2 {
        font-size: 36px;
        font-weight: 600;
        color: #cd8a3f;
    }
</style>
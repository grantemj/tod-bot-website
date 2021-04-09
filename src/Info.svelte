<script>
    export let serverCount
</script>

<div id="info">
    <img src="https://truthordarebot.xyz/PFP.png" alt="Profile pic" id="main-pfp">
    <h2>Currently in <code>{serverCount}</code> servers</h2>
</div>

<style>
    #info {
        width: 100%;
        text-align: center;
        padding-top: 225px;
        padding-bottom: 70px;
    }

    #main-pfp {
        border-radius: 50%;
        width: 350px;
        height: 350px;
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
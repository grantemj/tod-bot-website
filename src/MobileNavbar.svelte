<script>
    let opened = false

    function toggleMenu() {
        opened = !opened
    }
</script>

<main>
    <button id="mobile-menu" on:click={toggleMenu}></button>
    <div id="top-bar">
        <a href="https://discordapp.com/api/oauth2/authorize?client_id=692045914436796436&permissions=68608&scope=bot" target="_blank"><img src="https://truthordarebot.xyz/PFP.png" alt="Profile pic" id="pfp"></a>  
        <h1 id="title">Truth or Dare</h1>
    </div>
    <div id="dropdown" class={opened ? "menu-opened" : "menu-closed"}>
        <nav>
            <ul>
                <li>
                    <a href="https://truthordarebot.xyz" target="_self">Home</a>
                    <ul>
                        <li><a href="https://truthordarebot.xyz/#about-anchor" target="_self">About</a></li>
                        <li><a href="https://truthordarebot.xyz/#getting-started-anchor" target="_self">Getting Started</a></li>
                        <li><a href="https://truthordarebot.xyz/#commands-anchor" target="_self">Commands</a></li>
                        <li><a href="https://truthordarebot.xyz/#contact-anchor" target="_self">Contact</a></li>
                    </ul>
                </li>
                <li><a href="feedback" target="_self">Give Feedback</a></li>
                <li><a href="question_submit" target="_self">Submit Questions</a></li>
                <li><a href="survey" target="_self">Usage Survey</a></li>
            </ul>
        </nav>
    </div>
</main>

<style>
    main {
        position: absolute;
        width: 100%;
        background: #202122;
        color: #f4f1eb;
        top: 0px;
        left: 0px;
        z-index: 5;
    }

    #top-bar {
        position: absolute;
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 100%;
        background: #202122;
        color: #f4f1eb;
        top: 0px;
        left: 0px;
        z-index: 5;
    }

    #dropdown {
        position: absolute;
        top: 0;
        z-index: 6;
        transition: ease-out 0.35s;
        background: #202122;
        height: 100vh;
        width: 100vw;
    }

    .menu-opened {
        transform: translateY(0vh)
    }

    .menu-closed {
        transform: translateY(-100vh)
    }

    #mobile-menu {
        float: left;
        width: 60px;
        height: 60px;
        background-image: url("https://truthordarebot.xyz/mobile-menu.png");
        background-color: transparent;
        background-size: contain;
        border: none;
        margin-bottom: 0px;
        position: absolute;
        top: 10px;
        left: 15px;
        z-index: 10;
    }

    #pfp {
        float: left;
        border-radius: 50%;
        height: 60px;
        margin-left: 100px;
    }

    #title {
        float: left;
        font-weight: 500;
        font-size: 32px;
        margin-left: 20px;
    }

    nav {
        float: left;
    }

    nav ul {
        display: flex;
        flex-direction: column;
        padding-left: 50px;
        margin-top: 60px;
    }

    nav ul li {
        padding: 10px 25px 10px 25px;
        margin: 0px 0px 0px 0px;
        list-style: none;
        font-size: 24px;
        font-family: "Rubik";
        color: #f4f1eb;
        position: relative;
    }

    nav a:hover {
        color: #bab5ab;
    }

    nav ul li ul {
        padding-left: 20px;
        margin-top: 0px;
    }

    nav ul li ul li {
        font-size: 22px;
        font-weight: 300;
    }
</style>
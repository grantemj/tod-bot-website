<script>
    
</script>

<div id="desktop-navbar">
    <a href="https://discordapp.com/api/oauth2/authorize?client_id=692045914436796436&permissions=68608&scope=bot" target="_blank"><img src="https://truthordarebot.xyz/PFP.png" alt="Profile pic" id="pfp"></a>
    <h1 id="title">Truth or Dare</h1>
    <nav>
        <ul>
            <li id="home-nav">
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

<style>
    #desktop-navbar {
        position: absolute;
        width: 100%;
        background: #202122;
        color: #f4f1eb;
        top: 0px;
        left: 0px;
        z-index: 5;
    }

    #pfp {
        float: left;
        border-radius: 50%;
        height: 3.75rem;
        margin: 13px 30px 13px 35px;
    }

    #title {
        float: left;
        font-weight: 500;
        font-size: 2rem;
    }

    nav {
        float: right;
        background: #202122;
    }

    nav ul {
        display: flex;
        flex-direction: row;
        padding-left: 0px;
    }

    nav ul li {
        padding: 10px 25px 10px 25px;
        margin: 0px 0px 0px 0px;
        list-style: none;
        font-size: 1.5rem;
        font-family: "Rubik";
        color: #f4f1eb;
        position: relative;
    }

    #home-nav:hover > ul {
        animation: dropDown 150ms ease-in-out forwards;
        transform-origin: top center;
        visibility: visible;
    }

    #home-nav > ul {
        visibility: hidden;
    }

    #home-nav:hover > ul > li {
        visibility: visible;
    }

    #home-nav > ul > li {
        visibility: hidden;
    }

    @keyframes dropDown {
        0% {
            transform: scaleY(0);
        }
        1% {
            transform: scaleY(0.01);
        }
        100% {
            transform: scaleY(1);
        }
    }

    nav a:hover {
        color: #bab5ab;
    }

    nav ul li ul {
        position: absolute;
        top: 45px;
        left: 0px;
        background-color: #202122;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        z-index: 4;
        transform: translateY(-300px);
        padding-left: 10px;
    }

    nav ul li ul li {
        font-size: 1.675rem;
        font-weight: 300;
    }
</style>
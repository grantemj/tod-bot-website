<script>
    export let mobile

    function toggleMenu() {

    }
</script>

<main>
    {#if mobile}
        <img src="./mobile-menu.png" alt="mobile-menu" on:click={toggleMenu}>
    {/if}
    <nav>
        <ul>
            <li>
                <a href="https://truthordarebot.xyz" class="nav-link" target="_self" onclick="closeMenu()">Home</a>
                <ul>
                    <li><a href="https://truthordarebot.xyz/#about-anchor" class="nav-link" target="_self" onclick="closeMenu()">About</a></li>
                    <li><a href="https://truthordarebot.xyz/#getting-started-anchor" class="nav-link" target="_self" onclick="closeMenu()">Getting Started</a></li>
                    <li><a href="https://truthordarebot.xyz/#commands-anchor" class="nav-link" target="_self" onclick="closeMenu()">Commands</a></li>
                    <li><a href="https://truthordarebot.xyz/#contact-anchor" class="nav-link" target="_self" onclick="closeMenu()">Contact</a></li>
                </ul>
            </li>
            <li><a href="feedback" class="nav-link" target="_self" onclick="closeMenu()">Give Feedback</a></li>
            <li><a href="question_submit" class="nav-link" target="_self" onclick="closeMenu()">Submit Questions</a></li>
            <li><a href="survey" class="nav-link" target="_self" onclick="closeMenu()">Complete the Survey</a></li>
        </ul>
    </nav>
</main>

{#if mobile}
    <style>

    </style>
{:else}
    <style>
        main {
            position: absolute;
            width: 100%;
            background: hsl(204, 80%, 11%);
            color: white;
            top: 0px;
            left: 0px;
            z-index: 5;
        }

        nav {
            float: right;
        }

        nav ul {
            display: flex;
            flex-direction: row;
            padding-left: 0px;
        }

        nav li {
            padding: 10px 25px 10px 25px;
            margin: 0px 0px 0px 0px;
            list-style: none;
            font-size: 26px;
            font-family: "Rubik";
            color: #EEE;
        }
    
        nav a:hover {
            color: #AAA;
        }

        nav ul li ul {
            position: absolute;
            top: 50px;
            left: 0px;
            background-color: hsl(204, 80%, 11%);
            visibility: hidden;
            border-radius: 5px;
            display: flex;
            flex-direction: column;
        }

        nav ul li ul li {
            font-size: 22px;
            font-weight: 300;
        }
    </style>
{/if}
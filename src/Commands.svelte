<script>
    var selected;

    function hide() {
        this.children.item(1).style.visibility = "hidden"
        this.children.item(1).style.opacity = 0
    }

    function show() {
        this.nextElementSibling.style.visibility = "visible"
        this.nextElementSibling.style.opacity = 0.95
    }
</script>

<div id="commands">
    <h1 class="section-title">Commands</h1>
    <div class="row">
        <div class="column">
            <h2>Help Commands</h2>
            <ul>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>help</span>
                    <div class="tooltip" id="help">
                        <h3>Help Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+help [command]</b>: Lists all commands or gives info about a command.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>settings</span>
                    <div class="tooltip" id="settings">
                        <h3>Settings Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+settings</b>:  Lists the settings in the current channel. Use +enable and +disable to change settings.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>links</span>
                    <div class="tooltip" id="links">
                        <h3>Links Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+links</b>: Gives various links related to the bot, including the question submit form, feedback form, support server, how to add the bot to your own server, and more.</p>
                    </div>
                </li>
            </ul>
        </div>
        <div class="column">
            
        </div>
        <div class="column">
            
        </div>
    </div>
</div>

<style>
    h2 {
        font-size: 1.75rem;
        font-family: "Montserrat";
        font-weight: 400;
        text-decoration: underline;
    }

    .row {
        width: 70%;
        display: flex;
        flex-direction: row;
        margin-left: auto;
        margin-right: auto;
    }

    .column {
        width: 33.33%;
        text-align: center;
    }

    ul {
        padding: 0;
    }

    li {
        list-style: none;
        position: relative;
        margin: 20px 33.33% 20px 33.33%;
        color: #2d8bc0;
        font-size: 1.625rem;
        font-weight: 400;
    }

    span {
        padding: 10px;
    }

    .tooltip {
        background: #202122;
        border: 3px solid #2d3966;
        border-radius: 10px;
        position: absolute;
        top: calc(1em + 15px);
        left: -75%;
        visibility: hidden;
        width: 250%;
        z-index: 5;
        text-align: left;
        padding: 10px;
        color: #f4f1eb;
        transition: 0.2s;
    }

    .tooltip h3 {
        font-family: "Rubik";
        font-size: 1.5rem;
        color: #f4f1eb;
        font-weight: 500;
        margin-top: 0px;
        margin-bottom: 0px;
    }

    .tooltip h4 {
        font-family: "Rubik";
        font-size: 19px;
        text-decoration: underline;
        font-weight: 400;
        margin-top: 5px;
        margin-bottom: 0px;
    }

    .tooltip p {
        font-size: 0.875rem;
        font-weight: 400;
        margin: 5px 0px 0px 0px;
    }
</style>
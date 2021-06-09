<script>
    export let viewingMode

    var selected;

    function hide() {
        if (selected !== this.children.item(1).id) {
            this.children.item(1).style.visibility = "hidden"
            this.children.item(1).style.opacity = 0
        }
    }

    function show() {
        this.nextElementSibling.style.visibility = "visible"
        this.nextElementSibling.style.opacity = 0.95
    }

    function select() {
        let previouslySelected = document.getElementById(selected)
        if (previouslySelected) setTimeout(() => {previouslySelected.style.zIndex = 5}, 200)
        
        if (selected === this.nextElementSibling.id) {
            selected = null
            hideAll()
        } else {
            selected = this.nextElementSibling.id
            this.nextElementSibling.style.zIndex = 4
            hideAll()
        }
    }

    function hideAll() {
        document.querySelectorAll(".command").forEach(item => {
            hide.apply(item)
        })
    }
</script>

<div id="commands">
    <h1 class="section-title">Commands</h1>
    <div class="row {viewingMode}">
        <div class="column {viewingMode}">
            <h2 class={viewingMode}>Help Commands</h2>
            <ul>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>help</span>
                    <div class="tooltip" id="help">
                        <h3>Help Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+help [command]</b>: Lists all commands or gives info about a command.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>settings</span>
                    <div class="tooltip" id="settings">
                        <h3>Settings Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+settings</b>:  Lists the settings in the current channel. Use +enable and +disable to change settings.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>links</span>
                    <div class="tooltip" id="links">
                        <h3>Links Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+links</b>: Gives various links related to the bot, including the question submit form, feedback form, support server, how to add the bot to your own server, and more.</p>
                    </div>
                </li>
            </ul>
            <h2 class={viewingMode}>Miscellaneous Commands</h2>
            <ul>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>truthful</span>
                    <div class="tooltip" id="truthful">
                        <h3>Truthful Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+truthful [target]</b>: Uses semi-quasi-pseudo-random procedures to tell you how truthful a user is while answering questions.</p>
                      </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>stats</span>
                    <div class="tooltip" id="stats">
                        <h3>Stats Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+stats</b>: Lists various measures and statistics about the bot and its performance.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>ping</span>
                    <div class="tooltip" id="ping">
                        <h3>Ping Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+ping</b>: Displays the average ping between the bot and Discord's webservers.</p>
                    </div>
                </li>
            </ul>
        </div>
        <div class="column {viewingMode}">
            <h2 class={viewingMode}>Question Commands</h2>
            <ul>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>truth</span>
                    <div class="tooltip" id="truth">
                        <h3>Truth Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+truth [rating]</b>: Gives a random question that has to be answered truthfully.</p>
                        <h4>Arguments:</h4>
                        <p><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>dare</span>
                    <div class="tooltip" id="dare">
                        <h3>Dare Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+dare [rating] [type]</b>: Gives a dare that has to be completed.</p>
                        <h4>Arguments:</h4>
                        <p><b>d</b>: Gives a dare that is done over the internet or on a device.<br><b>irl</b>: Gives a dare that is done in real life/in person<br><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>wyr</span>
                    <div class="tooltip" id="wyr">
                        <h3>Would You Rather Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+wyr [rating]</b>: Gives a random 'Would You Rather' question to be answered.</p>
                        <h4>Arguments:</h4>
                        <p><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>nhie</span>
                    <div class="tooltip" id="nhie">
                        <h3>Never Have I Ever Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+nhie [rating]</b>: Gives a random 'Never Have I Ever' question to be answered.</p>
                        <h4>Arguments:</h4>
                        <p><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>paranoia</span>
                    <div class="tooltip" id="paranoia">
                        <h3>Paranoia Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+paranoia [target] [rating]</b>: Sends a paranoia question to the target, select the target by @ing them.</p>
                        <h4>Arguments:</h4>
                        <p><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>ans</span>
                    <div class="tooltip" id="ans">
                        <h3>Answer Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+ans [answer]</b>: Used to answer a paranoia question, can only be used in DMs. The brackets represent an argument, it is not required to enclose your answer in brackets. Example: Use '+ans John', not '+ans [John]'.</p>
                    </div>
                </li>
            </ul>
        </div>
        <div class="column {viewingMode}">
            <h2 class={viewingMode}>Utility Commands</h2>
            <ul>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>enable</span>
                    <div class="tooltip" id="enable">
                        <h3>Enable command</h3>
                        <h4>Usage:</h4>
                        <p><b>+enable [command] [rating]</b>: Enables the command/rating specified.</p>
                        <h4>Arguments:</h4>
                        <p><b>server</b>: Enables serverwide. If this argument is absent, the command/category will be enabled only in the channel the message was sent.<br><b>pg</b> / <b>pg13</b> / <b>r</b>: Enables the respective category for all commands, or can be added after a command to enable for that command only.<br><b>d</b> / <b>irl</b>: Enables the respective category for the dare command.<br><b>truth</b> / <b>dare</b> / <b>wyr</b> / <b>nhie</b> / <b>paranoia</b>: Enables pg and pg13 categories for the respective command, as well as d and irl categories if dare is specified.
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>disable</span>
                    <div class="tooltip" id="disable">
                        <h3>Disable command</h3>
                        <h4>Usage:</h4>
                        <p><b>+disable [command] [rating]</b>: Disables the command/rating specified.</p>
                        <h4>Arguments:</h4>
                        <p><b>server</b>: Disables serverwide. If this argument is absent, the command/category will be disabled only in the channel the message was sent.<br><b>pg</b> / <b>pg13</b> / <b>r</b>: Disables the respective category for all commands, or can be added after a command to disable for that command only.<br><b>d</b> / <b>irl</b>: Disables the respective category for the dare command.<br><b>truth</b> / <b>dare</b> / <b>wyr</b> / <b>nhie</b> / <b>paranoia</b>: Disables pg and pg13 categories for the respective command, as well as d and irl categories if dare is specified.
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>mute</span>
                    <div class="tooltip" id="mute">
                        <h3>Mute Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+mute</b>: Used to mute the bot in the channel the message was sent. When muted, the bot will not respond to any commands.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>unmute</span>
                    <div class="tooltip" id="unmute">
                        <h3>Unmute Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+unmute</b>: Used to unmute the bot in the channel the message was sent. When muted, the bot will not respond to any commands.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show} on:click={select}>prefix</span>
                    <div class="tooltip" id="prefix">
                        <h3>Prefix Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+prefix [new prefix]</b>: Used to set a new prefix for the bot. Standard '+' prefix will be used in DMs. New prefix must either contain +, !, $, %, ^, &, -, &lt;, or &gt;, or be between 4 and 8 characters long.</p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</div>

<style>
    #commands {
        padding-top: 70px;
    }

    h2 {
        font-size: 1.75rem;
        font-family: "Montserrat";
        font-weight: 400;
        text-decoration: underline;
    }

    .h2.mobile {
        display: inline-block;
    }

    .row {
        width: 70%;
        display: flex;
        flex-direction: row;
        margin-left: auto;
        margin-right: auto;
    }

    .row.mobile {
        width: 95%;
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .column {
        width: 33.33%;
        text-align: center;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .column.mobile {
        width: 100%;
    }

    ul {
        padding: 0;
        display: flex;
        flex-direction: column;
    }

    li {
        list-style: none;
        position: relative;
        margin: 1rem auto 1rem auto;
        color: var(--light-blue);
        font-size: 1.625rem;
        font-weight: 400;
        text-align: center;
        display: inline-block;
        font-family: monospace;
    }

    span {
        padding: 0.625rem;
        cursor: pointer;
    }

    .tooltip {
        background: var(--black);
        border: 3px solid var(--dark-blue);
        border-radius: 10px;
        position: absolute;
        top: calc(1em + 1rem);
        left: 50%;
        transform: translateX(-50%);
        visibility: hidden;
        width: 250%;
        z-index: 5;
        text-align: left;
        padding: 0.625rem;
        color: var(--white);
        transition: 0.2s;
    }

    .tooltip h3 {
        font-family: "Rubik";
        font-size: 1.5rem;
        color: var(--white);
        font-weight: 500;
        margin-top: 0px;
        margin-bottom: 0px;
    }

    .tooltip h4 {
        font-family: "Rubik";
        font-size: 1.1875rem;
        text-decoration: underline;
        font-weight: 400;
        margin-top: 0.3125rem;
        margin-bottom: 0px;
    }

    .tooltip p {
        font-size: 0.875rem;
        font-weight: 400;
        margin: 0.3125rem 0px 0px 0px;
        font-family: 'Rubik';
    }
</style>
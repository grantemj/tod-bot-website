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
            <h2>Miscellaneous Commands</h2>
            <ul>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>truthful</span>
                    <div class="tooltip" id="truthful">
                        <h3>Truthful Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+truthful [target]</b>: Uses semi-quasi-pseudo-random procedures to tell you how truthful a user is while answering questions.</p>
                      </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>stats</span>
                    <div class="tooltip" id="stats">
                        <h3>Stats Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+stats</b>: Lists various measures and statistics about the bot and its performance.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>ping</span>
                    <div class="tooltip" id="ping">
                        <h3>Ping Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+ping</b>: Displays the average ping between the bot and Discord's webservers.</p>
                    </div>
                </li>
            </ul>
        </div>
        <div class="column">
            <h2>Question Commands</h2>
            <ul>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>truth</span>
                    <div class="tooltip" id="truth">
                        <h3>Truth Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+truth [rating]</b>: Gives a random question that has to be answered truthfully.</p>
                        <h4>Arguments:</h4>
                        <p><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>dare</span>
                    <div class="tooltip" id="dare">
                        <h3>Dare Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+dare [rating] [type]</b>: Gives a dare that has to be completed.</p>
                        <h4>Arguments:</h4>
                        <p><b>d</b>: Gives a dare that is done over the internet or on a device.<br><b>irl</b>: Gives a dare that is done in real life/in person<br><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>wyr</span>
                    <div class="tooltip" id="wyr">
                        <h3>Would You Rather Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+wyr [rating]</b>: Gives a random 'Would You Rather' question to be answered.</p>
                        <h4>Arguments:</h4>
                        <p><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>nhie</span>
                    <div class="tooltip" id="nhie">
                        <h3>Never Have I Ever Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+nhie [rating]</b>: Gives a random 'Never Have I Ever' question to be answered.</p>
                        <h4>Arguments:</h4>
                        <p><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>paranoia</span>
                    <div class="tooltip" id="paranoia">
                        <h3>Paranoia Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+paranoia [target] [rating]</b>: Sends a paranoia question to the target, select the target by @ing them.</p>
                        <h4>Arguments:</h4>
                        <p><b>pg</b>: Gives a 'PG' question (no inapporopriate content.)<br><b>pg13</b>: Gives a 'PG13' rated question (may be suggestive, many have to with dating/relationships.)<br><b>r</b>: Gives a 'R' rated question (most likely overtly sexual)</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>ans</span>
                    <div class="tooltip" id="ans">
                        <h3>Answer Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+ans [answer]</b>: Used to answer a paranoia question, can only be used in DMs. The brackets represent an argument, it is not required to enclose your answer in brackets. Example: Use '+ans John', not '+ans [John]'.</p>
                    </div>
                </li>
            </ul>
        </div>
        <div class="column">
            <h2>Utility Commands</h2>
            <ul>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>enable</span>
                    <div class="tooltip" id="enable">
                        <h3>Enable command</h3>
                        <h4>Usage:</h4>
                        <p><b>+enable [command] [rating]</b>: Enables the command/rating specified.</p>
                        <h4>Arguments:</h4>
                        <p><b>server</b>: Enables serverwide. If this argument is absent, the command/category will be enabled only in the channel the message was sent.<br><b>pg</b>: Enables pg category for all commands, or can be added after a command to enable for that command only.<br><b>pg13</b>: Enables pg13 category for all commands, or can be added after a command to enable for that command only.<br><b>r</b>: Enables r category for all commands, or can be added after a command to enable for that command only.<br><b>d</b>: Enables digital category for the dare command.<br><b>irl</b>: Enables real life category for the dare command.<br><b>truth</b>: Enables all categories for the truth command.<br><b>dare</b>: Enables all categories for the dare command.<br><b>wyr</b>: Enables all categories for the Would You Rather command.<br><b>nhie</b>: Enables all categories for the Never Have I Ever command.<br><b>paranoia</b>: Enables all categories for the paranoia command.
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>disable</span>
                    <div class="tooltip" id="disable">
                        <h3>Disable command</h3>
                        <h4>Usage:</h4>
                        <p><b>+disable [command] [rating]</b>: Disables the command/rating specified.</p>
                        <h4>Arguments:</h4>
                        <p><b>server</b>: Disables serverwide. If this argument is absent, the command/category will be disabled only in the channel the message was sent.<br><b>pg</b>: Disables pg category for all commands, or can be added after a command to disable for that command only.<br><b>pg13</b>: Disables pg13 category for all commands, or can be added after a command to disable for that command only.<br><b>r</b>: Disables r category for all commands, or can be added after a command to disable for that command only.<br><b>d</b>: Disables digital category for the dare command.<br><b>irl</b>: Disables real life category for the dare command.<br><b>truth</b>: Disables all categories for the truth command.<br><b>dare</b>: Disables all categories for the dare command.<br><b>wyr</b>: Disables all categories for the Would You Rather command.<br><b>nhie</b>: Disables all categories for the Never Have I Ever command.<br><b>paranoia</b>: Disables all categories for the paranoia command.
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>mute</span>
                    <div class="tooltip" id="mute">
                        <h3>Mute Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+mute</b>: Used to mute the bot in the channel the message was sent. When muted, the bot will not respond to any commands.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>unmute</span>
                    <div class="tooltip" id="unmute">
                        <h3>Unmute Command</h3>
                        <h4>Usage:</h4>
                        <p><b>+unmute</b>: Used to unmute the bot in the channel the message was sent. When muted, the bot will not respond to any commands.</p>
                    </div>
                </li>
                <li class="command" on:mouseleave={hide}><span on:mouseover={show}>prefix</span>
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

    @media (max-width: 480px) {
        .row {
            width: 95%;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        h2 {
            display: inline-block;
        }
    }

    .column {
        width: 33.33%;
        text-align: center;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    ul {
        padding: 0;
        display: flex;
        flex-direction: column;
    }

    li {
        list-style: none;
        position: relative;
        margin: 15px auto 15px auto;
        color: #2d8bc0;
        font-size: 1.625rem;
        font-weight: 400;
        text-align: center;
        display: inline-block;
    }

    span {
        padding: 10px;
        cursor: pointer;
    }

    .tooltip {
        background: #202122;
        border: 3px solid #2d3966;
        border-radius: 10px;
        position: absolute;
        top: calc(1em + 15px);
        left: 50%;
        transform: translateX(-50%);
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
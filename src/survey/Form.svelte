<script>

</script>

<form action="/form_submit" method="POST" id="form" autocomplete="off">
    <h3>Completing this survey helps the developers better understand how you use the bot and what the most important things to improve are. Feel free to answer as many or as few of the questions as you like, it's okay to leave some empty.</h3>
    <input name="form-name" value="Survey" id="form-name">
    <h2>Usage Habits</h2>
    <ul>
        <li>
            <h3 class="form-question">How often do you use the bot?</h3>
            <ul>
                <li>
                    <input type="radio" name="frequency" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="multiple-times-a-day" class="radio-checkmark-label">Multiple times a day
                        <input type="radio" id="multiple-times-a-day" name="frequency" value="Multiple times a day">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="once-a-day" class="radio-checkmark-label">Once a day
                        <input type="radio" id="once-a-day" name="frequency" value="Once a day">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="few-times-a-week" class="radio-checkmark-label">A few times a week
                        <input type="radio" id="few-times-a-week" name="frequency" value="A few times a week">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="once-a-week" class="radio-checkmark-label">Once a week
                        <input type="radio" id="once-a-week" name="frequency" value="Once a week">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="few-times-a-month" class="radio-checkmark-label">A few times a month
                        <input type="radio" id="few-times-a-month" name="frequency" value="A few times a month">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="once-a-month" class="radio-checkmark-label">Once a month or less
                        <input type="radio" id="once-a-month" name="frequency" value="Once a month or less">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question">How many of the servers that you are in have the bot in them?</h3>
            <ul>
                <li>
                    <input type="radio" name="how-many-servers" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="one-server" class="radio-checkmark-label">1
                        <input type="radio" id="one-server" name="how-many-servers" value="One server">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="two-to-four-servers" class="radio-checkmark-label">2-4
                        <input type="radio" id="two-to-four-servers" name="how-many-servers" value="Two to four servers">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="five-to-eight-servers" class="radio-checkmark-label">5-8
                        <input type="radio" id="five-to-eight-servers" name="how-many-servers" value="Five to eight servers">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="more-than-9-servers" class="radio-checkmark-label">9+
                        <input type="radio" id="more-than-9-servers" name="how-many-servers" value="More than 9 servers">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <label for="server-member-count" class="form-question">Approximately many people are there in these servers, and how many of them are active often?</label>
            <input id="server-member-count" name="Approximately many people are there in these servers, and how many of them are active often?" type="text">
        </li>
        <li>
            <label for="concurrent-users" class="form-question">On average, while the bot is being used, how many people are there using the bot at a time?</label>
            <input id="concurrent-users" name="On average, while the bot is being used, how many people are there using the bot at a time?" type="text">
        </li>
        <li>
            <h3 class="form-question">Check all of the following commands/ratings/categories that are enabled in the servers you use the bot in.</h3>
            <ul>
                <li>
                    <label for="truth-enabled" class="checkmark-label">Truth
                        <input type="checkbox" id="truth-enabled" name="enabled" value="Truth">
                        <span class="checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="dare-enabled" class="checkmark-label">Dare
                        <input type="checkbox" id="dare-enabled" name="enabled" value="Dare">
                        <span class="checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="paranoia-enabled" class="checkmark-label">Paranoia
                        <input type="checkbox" id="paranoia-enabled" name="enabled" value="Paranoia">
                        <span class="checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="nhie-enabled" class="checkmark-label">Never Have I Ever
                        <input type="checkbox" id="nhie-enabled" name="enabled" value="nhie">
                        <span class="checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="wyr-enabled" class="checkmark-label">Would You Rather
                        <input type="checkbox" id="wyr-enabled" name="enabled" value="wyr">
                        <span class="checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="pg-enabled" class="checkmark-label">PG Questions
                        <input type="checkbox" id="pg-enabled" name="enabled" value="pg">
                        <span class="checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="pg13-enabled" class="checkmark-label">PG13 Questions
                        <input type="checkbox" id="pg13-enabled" name="enabled" value="pg13">
                        <span class="checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="r-enabled" class="checkmark-label">R questions
                        <input type="checkbox" id="r-enabled" name="enabled" value="r">
                        <span class="checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <label for="language" class="form-question">Does your server normally use a language other than English, and if so, what language?</label>
            <input id="language" name="Does your server normally use a language other than English, and if so, what language?" type="text">
        </li>
    </ul>
    <h2>Bot Questions</h2>
    <ul>
        <li>
            <label for="number-truth-questions" class="form-question">How many truth questions would you guess the bot has?</label>
            <input id="number-truth-questions" name="How many truth questions would you guess the bot has?" type="text">
        </li>
        <li>
            <label for="number-dare-questions" class="form-question">How many dare questions would you guess the bot has?</label>
            <input id="number-dare-questions" name="How many dare questions would you guess the bot has?" type="text">
        </li>
        <li>
            <label for="number-paranoia-questions" class="form-question">How many Paranoia questions would you guess the bot has?</label>
            <input id="number-paranoia-questions" name="How many Paranoia questions would you guess the bot has?" type="text">
        </li>
        <li>
            <label for="number-wyr-questions" class="form-question">How many Would You Rather questions would you guess the bot has?</label>
            <input id="number-wyr-questions" name="How many Would You Rather questions would you guess the bot has?" type="text">
        </li>
        <li>
            <label for="number-nhie-questions" class="form-question">How many Never Have I Ever questions would you guess the bot has?</label>
            <input id="number-nhie-questions" name="How many Never Have I Ever questions would you guess the bot has?" type="text">
        </li>
        <li>
            <label for="percent-seen" class="form-question">Out of all the questions the bot has, what percentage of them do you think you've seen or answered?</label>
            <input id="percent-seen" name="Out of all the questions the bot has, what percentage of them do you think you've seen or answered?" type="text">
        </li>
        <li>
            <h3 class="form-question">Agree or Disagree: The bot repeats questions too often.</h3>
            <ul>
                <li>
                    <input type="radio" name="repetition" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="strongly-disagree-1" class="radio-checkmark-label">Strongly disagree
                        <input type="radio" id="strongly-disagree-1" name="repetition" value="Strongly disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="disagree-1" class="radio-checkmark-label">Disagree
                        <input type="radio" id="disagree-1" name="repetition" value="Disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="agree-1" class="radio-checkmark-label">Agree
                        <input type="radio" id="agree-1" name="repetition" value="Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="strongly-agree-1" class="radio-checkmark-label">Strongly Agree
                        <input type="radio" id="strongly-agree-1" name="repetition" value="Strongly Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question">Agree or Disagree: The bot's questions are well phrased and high-quality.</h3>
            <ul>
                <li>
                    <input type="radio" name="quality-questions" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="strongly-disagree-2" class="radio-checkmark-label">Strongly disagree
                        <input type="radio" id="strongly-disagree-2" name="quality-questions" value="Strongly disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="disagree-2" class="radio-checkmark-label">Disagree
                        <input type="radio" id="disagree-2" name="quality-questions" value="Disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="agree-2" class="radio-checkmark-label">Agree
                        <input type="radio" id="agree-2" name="quality-questions" value="Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="strongly-agree-2" class="radio-checkmark-label">Strongly Agree
                        <input type="radio" id="strongly-agree-2" name="quality-questions" value="Strongly Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question">Agree or Disagree: The bot's questions cause a lot of interesting conversation.</h3>
            <ul>
                <li>
                    <input type="radio" name="interesting-questions" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="strongly-disagree-3" class="radio-checkmark-label">Strongly disagree
                        <input type="radio" id="strongly-disagree-3" name="interesting-questions" value="Strongly disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="disagree-3" class="radio-checkmark-label">Disagree
                        <input type="radio" id="disagree-3" name="interesting-questions" value="Disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="agree-3" class="radio-checkmark-label">Agree
                        <input type="radio" id="agree-3" name="interesting-questions" value="Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="strongly-agree-3" class="radio-checkmark-label">Strongly Agree
                        <input type="radio" id="strongly-agree-3" name="interesting-questions" value="Strongly Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
    </ul>
    <h2>Publicity</h2>
    <ul>
        <li>
            <h3 class="form-question">How did you first find out about the bot?</h3>
            <ul>
                <li>
                    <input type="radio" name="discovered" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="google" class="radio-checkmark-label">Through Google
                        <input type="radio" id="google" name="discovered" value="Through Google">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="website" class="radio-checkmark-label">By finding the website online
                        <input type="radio" id="website" name="discovered" value="By finding the website online">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="recommendation" class="radio-checkmark-label">A friend recommended it to me
                        <input type="radio" id="recommendation" name="discovered" value="A friend recommended it to me">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="added-to-server" class="radio-checkmark-label">It was added to a server that I'm in
                        <input type="radio" id="added-to-server" name="discovered" value="It was added to a server that I'm in">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="bot-listing" class="radio-checkmark-label">Through a bot listing site like top.gg
                        <input type="radio" id="bot-listing" name="discovered" value="Through a bot listing site like top.gg">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question">Have you joined the support server, and if so, for what reason?</h3>
            <ul>
                <li>
                    <input type="radio" name="support-server" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="not-joined" class="radio-checkmark-label">No
                        <input type="radio" id="not-joined" name="support-server" value="No">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="setup-help" class="radio-checkmark-label">Yes, I needed help setting up the bot
                        <input type="radio" id="setup-help" name="support-server" value="Yes, I needed help setting up the bot">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="broken" class="radio-checkmark-label">Yes, the bot was down or offline when I tried to use it
                        <input type="radio" id="broken" name="support-server" value="Yes, the bot was down or offline when I tried to use it">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="feature-questions" class="radio-checkmark-label">Yes, I wanted to ask questions about the bot and its features
                        <input type="radio" id="feature-questions" name="support-server" value="Yes, I wanted to join a community of people who also enjoy the bot">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="community" class="radio-checkmark-label">Yes, I wanted to join a community of people who also enjoy the bot
                        <input type="radio" id="community" name="support-server" value="Yes, I wanted to join a community of people who also enjoy the bot">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question">Have you visited the bot's website?</h3>
            <ul>
                <li>
                    <input type="radio" name="website" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="not-visited" class="radio-checkmark-label">No, I didn't know the bot had a website
                        <input type="radio" id="not-visited" name="website" value="No, I didn't know the bot had a website">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="seen-not-visited" class="radio-checkmark-label">No, but I've heard about it or seen a link to it before
                        <input type="radio" id="seen-not-visited" name="website" value="No, but I've heard about it or seen a link to it before">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="to-submit" class="radio-checkmark-label">Yes, I went to give feedback or submit questions
                        <input type="radio" id="to-submit" name="website" value="Yes, I went to give feedback or submit questions">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="command-help" class="radio-checkmark-label">Yes, I wanted help with the bot's commands
                        <input type="radio" id="command-help" name="website" value="Yes, I wanted help with the bot's commands">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="out-of-interest" class="radio-checkmark-label">Yes, I just wanted to see what it looked like
                        <input type="radio" id="out-of-interest" name="website" value="Yes, I just wanted to see what it looked like">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question">Were you aware you can submit your own questions to be used by the bot??</h3>
            <ul>
                <li>
                    <input type="radio" name="aware-of-submission" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="submitted" class="radio-checkmark-label">Yes, I've submitted questions before
                        <input type="radio" id="submitted" name="aware-of-submission" value="Yes, I've submitted questions before">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="aware-not-submitted" class="radio-checkmark-label">Yes, but I haven't submitted any
                        <input type="radio" id="aware-not-submitted" name="aware-of-submission" value="Yes, but I haven't submitted any">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="not-aware-wants-to" class="radio-checkmark-label">No, but I'd like to submit some questions
                        <input type="radio" id="not-aware-wants-to" name="aware-of-submission" value="No, but I'd like to submit some questions">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="not-aware-not-willing" class="radio-checkmark-label">No, but I don't want to submit any questions
                        <input type="radio" id="not-aware-not-willing" name="aware-of-submission" value="No, but I don't want to submit any questions">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
    </ul>
    <h2>User Experience</h2>
    <ul>
        <li>
            <h3 class="form-question">Agree or Disagree: The bot's commands are intuitive and easy to learn.</h3>
            <ul>
                <li>
                    <input type="radio" name="intuitive" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="strongly-disagree-4" class="radio-checkmark-label">Strongly disagree
                        <input type="radio" id="strongly-disagree-4" name="intuitive" value="Strongly disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="disagree-4" class="radio-checkmark-label">Disagree
                        <input type="radio" id="disagree-4" name="intuitive" value="Disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="agree-4" class="radio-checkmark-label">Agree
                        <input type="radio" id="agree-4" name="intuitive" value="Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="strongly-agree-4" class="radio-checkmark-label">Strongly Agree
                        <input type="radio" id="strongly-agree-4" name="intuitive" value="Strongly Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question">Agree or Disagree: The bot's messages are easy to read and understand.</h3>
            <ul>
                <li>
                    <input type="radio" name="readable" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="strongly-disagree-5" class="radio-checkmark-label">Strongly disagree
                        <input type="radio" id="strongly-disagree-5" name="readable" value="Strongly disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="disagree-5" class="radio-checkmark-label">Disagree
                        <input type="radio" id="disagree-5" name="readable" value="Disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="agree-5" class="radio-checkmark-label">Agree
                        <input type="radio" id="agree-5" name="readable" value="Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="strongly-agree-5" class="radio-checkmark-label">Strongly Agree
                        <input type="radio" id="strongly-agree-5" name="readable" value="Strongly Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question">Agree or Disagree: The help command solves my problems when I'm confused about how to use the bot.</h3>
            <ul>
                <li>
                    <input type="radio" name="help-helpful" value="" style="display: none;" checked>
                </li>
                <li>
                    <label for="strongly-disagree-6" class="radio-checkmark-label">Strongly disagree
                        <input type="radio" id="strongly-disagree-6" name="help-helpful" value="Strongly disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="disagree-6" class="radio-checkmark-label">Disagree
                        <input type="radio" id="disagree-6" name="help-helpful" value="Disagree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="agree-6" class="radio-checkmark-label">Agree
                        <input type="radio" id="agree-6" name="help-helpful" value="Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="strongly-agree-6" class="radio-checkmark-label">Strongly Agree
                        <input type="radio" id="strongly-agree-6" name="help-helpful" value="Strongly Agree">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
    </ul>
    <a id="submit-parent"><input type="submit" class="button" id="submit"></a>
</form>

<style>
    h2 {
        font-size: 35px;
        text-decoration: underline;
        font-family: "Montserrat";
        margin-top: 2em;
    }

    h3 {
        font-size: 20px;
        font-weight: normal;
        font-family: "Rubik";
    }

    form {
        display: inline-block;
        text-align: left;
        font-family: 'Rubik';
    }

    form ul {
        padding-left: 0px;
    }

    form ul li {
        list-style: none;
        font-size: 1.25rem;
    }

    form > ul > li {
        margin-top: 1.875rem;
        margin-bottom: 1.875rem;
    }

    .form-question {
        font-weight: 500;
        font-size: 1.375rem;
        margin: 0;
    }

    form ul li ul {
        margin-top: 1.25rem;
        margin-left: 1.25rem;
    }

    #form-name {
        display: none;
    }

    input[type="text"] {
        background: var(--black);
        color: var(--white);
        height: 2em;
        width: 30em;
        max-width: 80%;
        border: solid 3px var(--dark-blue);
        border-radius: 9px;
        margin-top: 1rem;
        font-size: 1rem;
    }

    .checkmark-label {
        display: block;
        position: relative;
        cursor: pointer;
        user-select: none;
        text-indent: 2em;
        margin-bottom: 12px;
    }

    .checkmark-label input {
        position: absolute;
        opacity: 0;
        cursor: pointer;
        height: 0;
        width: 0;
    }

    .checkmark {
        display: inline-block;
        position: absolute;
        top: 3px;
        left: 5px;
        height: 0.9em;
        width: 0.9em;
        background-color: var(--black);
        border: solid 2px var(--dark-blue);
        border-radius: 0.1em;
    }

    .checkmark-label:hover input ~ .checkmark {
        border-color: var(--orange);
    }

    .checkmark::after {
        content: "";
        position: absolute;
        display: none;
    }

    .checkmark-label input:checked ~ .checkmark::after {
        display: inline-block;
    }

    .checkmark-label .checkmark::after {
        left: 0.2em;
        top: 0.2em;
        width: 0.5em;
        height: 0.5em;
        background-color: var(--orange);
    }

    .radio-checkmark-label {
        display: block;
        position: relative;
        padding-left: 2.25rem;
        margin-bottom: 0.75rem;
        cursor: pointer;
        font-size: 1.25rem;
        user-select: none;
    }

    .radio-checkmark-label input {
        position: absolute;
        opacity: 0;
        cursor: pointer;
        height: 0;
        width: 0;
    }

    .radio-checkmark {
        position: absolute;
        top: 0;
        left: 0;
        height: 0.9em;
        width: 0.9em;
        background-color: var(--black);
        border: 2px solid var(--dark-blue);
        border-radius: 50%;
    }

    .radio-checkmark-label:hover input ~ .radio-checkmark {
        border-color: var(--orange);
    }
  
    .radio-checkmark:after {
        content: "";
        position: absolute;
        display: none;
    }
  
    .radio-checkmark-label input:checked ~ .radio-checkmark:after {
        display: block;
    }
  
    .radio-checkmark-label .radio-checkmark:after {
        top: 0.2em;
        left: 0.2em;
        width: 0.5em;
        height: 0.5em;
        border-radius: 50%;
        background: var(--orange);
    }

    input:focus {
        outline: none;
    }

    input[type="submit"] {
        background: var(--black);
        color: var(--white);
        font-family: "Rubik";
        font-size: 1.25rem;
        border: solid 3px var(--dark-blue);
        border-radius: 9px;
        padding: 0.4em;
        cursor: pointer;
    }

    input[type="submit"]:disabled {
        color: #BBB;
        border-width: 1px;
        margin-top: 2px;
        margin-left: 2px;
        cursor: default;
    }
</style>
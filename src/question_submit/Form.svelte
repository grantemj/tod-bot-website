<script>
    var supportServer = false

    var questionInput
    var formValid
    
    function validateForm() {
        formValid = (
            questionInput?.length > 10 
            && [...document.querySelectorAll('input[name="type"]')].some(item => item.checked)
            && [...document.querySelectorAll('input[name="rating"]')].some(item => item.checked)
        )
    }
</script>

<form action="/form_submit" method="POST" id="form" autocomplete="off" on:input={validateForm}>
    <input name="form-name" value="Question Submit" id="form-name">
    <ul>
        <li>
            <h3 for="question" class="form-question">What question would you like added?</h3>
            <input id="question" name="Question" type="text" required="" bind:value={questionInput}>
        </li>
        <li>
            <h3 class="form-question" for="type">What kind of question is this?</h3>
            <ul>
                <li>
                    <input type="radio" name="type" value="" style="display: none;" checked="">
                </li>
                <li>
                    <label for="truth" class="radio-checkmark-label">Truth Question
                        <input type="radio" id="truth" name="type" value="truth" required="">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="dare" class="radio-checkmark-label">Dare
                        <input type="radio" id="dare" name="type" value="dare" required="">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="wyr" class="radio-checkmark-label">Would You Rather Question
                        <input type="radio" id="wyr" name="type" value="wyr" required="">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="nhie" class="radio-checkmark-label">Never Have I Ever Prompt
                        <input type="radio" id="nhie" name="type" value="nhie" required="">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="paranoia" class="radio-checkmark-label">Paranoia Question
                        <input type="radio" id="paranoia" name="type" value="paranoia" required="">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <h3 class="form-question" for="rating">What is the rating of your question?</h3>
            <ul>
                <li>
                    <input type="radio" name="rating" value="" style="display: none;" checked="">
                </li>
                <li>
                    <label for="pg" class="radio-checkmark-label">pg
                        <input type="radio" id="pg" name="rating" value="pg" required="">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="pg13" class="radio-checkmark-label">pg13
                        <input type="radio" id="pg13" name="rating" value="pg13" required="">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
                <li>
                    <label for="r" class="radio-checkmark-label">r
                        <input type="radio" id="r" name="rating" value="r" required="">
                        <span class="radio-checkmark"></span>
                    </label>
                </li>
            </ul>
        </li>
        <li>
            <label for="in-support-server" id="checkmark-label">Are you a member of the Truth or Dare Bot support server?
                <input type="checkbox" id="in-support-server" name="User in support server" bind:checked={supportServer}>
                <span class="checkmark"></span>
            </label>
            {#if supportServer}
                <div id="username-div">
                    <label for="username" id="username-label">If you would like the Question Submitter role, enter your Discord username in the box below.</label>
                    <input type="text" id="username" name="User username">
                </div>
            {/if}
        </li>
    </ul>
    <a id="submit-parent"><input type="submit" class="button" id="submit" disabled={!formValid}></a>
</form>

<style>
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

    #checkmark-label {
        display: block;
        position: relative;
        cursor: pointer;
        user-select: none;
        text-indent: 2em;
    }

    #in-support-server {
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

    #checkmark-label:hover input ~ .checkmark {
        border-color: var(--orange);
    }

    .checkmark::after {
        content: "";
        position: absolute;
        display: none;
    }

    #in-support-server:checked ~ .checkmark::after {
        display: inline-block;
    }

    #checkmark-label .checkmark::after {
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

    #username-div {
        margin-top: 0.8em;
        margin-left: 2em;
    }

    #username-div label {
        font-weight: 400;
        font-size: 1.25rem;
    }

    input[disabled] {
        pointer-events: none;
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
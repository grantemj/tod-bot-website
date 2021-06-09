<script>
    var supportServer = false

    var experienceInput, complaintInput, enjoyInput, featureInput
    var formValid

    function validateForm() {
        formValid = (
            [...document.querySelectorAll("textarea")].some(item => item.value?.length > 10)
        )
    }
</script>

<form action="/form_submit" method="POST" id="form" autocomplete="off" on:input={validateForm}>
    <input name="form-name" value="Feedback" id="form-name">
    <ul>
        <li>
            <label for="experience" class="form-question">How is your overall experience using this bot?</label>
            <textarea id="experience" name="User Experience" maxlength="1000" bind:value={experienceInput}></textarea>
        </li>
        <li>
            <label for="complaints" class="form-question">What are some complaints you have regarding your experience using the bot?</label>
            <textarea id="complaints" name="User Complaints" maxlength="1000" bind:value={complaintInput}></textarea>
        </li>
        <li>
            <label for="enjoy" class="form-question">What are some things the bot does well or things you enjoy about the bot?</label>
            <textarea id="enjoy" name="User Enjoys" maxlength="1000" bind:value={enjoyInput}></textarea>
        </li>
        <li>
            <label for="new-features" class="form-question">What are some features you would like to see added to the bot?</label>
            <textarea id="new-features" name="Feature Suggestions" maxlength="1000" bind:value={featureInput}></textarea>
        </li>
        <li>
            <label for="in-support-server" id="checkmark-label">Are you in the Truth or Dare Bot support server and would like the "Feedback Giver" role?
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

    textarea {
        background: var(--black);
        color: var(--white);
        height: 8em;
        width: 30em;
        max-width: 80%;
        border: solid 3px var(--dark-blue);
        border-radius: 9px;
        margin-top: 1em;
        margin-left: 1em;
        font-size: 1rem;
        resize: none;
        
    }

    textarea::-webkit-scrollbar {
        width: 5px;
    }

    textarea::-webkit-scrollbar-button {
        display: none;
    }

    textarea::-webkit-scrollbar-track {
        background: transparent;
    }

    textarea::-webkit-scrollbar-thumb {
        background: var(--orange);
        width: 2px;
        border-radius: 2px;
    }

    textarea::-webkit-scrollbar-track-piece:start {
        background: transparent;
        margin-top: 0.2em;
    }

    textarea::-webkit-scrollbar-track-piece:end {
        background: transparent;
        margin-bottom: 0.2em;
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

    textarea:focus {
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
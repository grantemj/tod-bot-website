<script>

</script>

<form action="/form-submit" method="POST" id="form">
    <input name="form-name" value="Question Submit" id="form-name">
      <ul>
        <li>
          <label for="question" class="form-question">What question would you like added?</label><br>
          <input id="question" name="Question" type="text" required="">
        </li>
        <li>
          <label class="form-question" for="type">What kind of question is this?</label><br>
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
          <label class="form-question" for="rating">What is the rating of your question?</label><br>
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
          <label for="in-support-server" id="checkmark-label" class="form-question" style="text-indent: 33px;">Are you in the Truth or Dare Bot support server and would like the "Feedback Giver" role?
            <input type="checkbox" id="in-support-server" name="User in support server">
            <span class="checkmark"></span>
          </label>
          <div id="username-div">
            <label for="username" id="username-label" class="form-question">What is your Discord username?</label><br>
            <input type="text" id="username" name="User username">
          </div>
        </li>
      </ul>
      <a id="submit-parent"><input type="submit" class="button" id="submit" onclick="handleSubmit()" disabled=""></a>
      <p id="warning">The form isn't full enough to submit yet.</p>
</form>

<style>
    input[type="submit"] {
        background: #202122;
        color: #f4f1eb;
        font-family: "Rubik";
        font-size: 1.25rem;
        border: solid 3px #2d3966;
        border-radius: 9px;
    }
</style>
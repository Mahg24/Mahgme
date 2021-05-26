<form>
  <h1>Contact me</h1>
  <input type="text" placeholder="Email" />
  <textarea
    name=""
    placeholder="Arremangala arrempujala"
    id=""
    cols="30"
    rows="10"
  />
  <input type="submit" value="Send" />
</form>

<style>
  form {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 40vw;
  }
  form input,
  textarea {
    width: calc(100% - 1rem);

    margin: 5px;
    font-family: "Nunito", sans-serif;
    font-size: 16px;
  }
</style>

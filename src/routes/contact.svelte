<script>
  function OpenModal() {
    var modal = document.getElementById("myModal");
    modal.style.display = "block";
  }
  function CloseModal() {
    var modal = document.getElementById("myModal");
    modal.style.display = "None";
  }
  async function validate() {
    let email = document.querySelector("#email");
    let message = document.querySelector("#message");
    let validation = true;
    if (email.value == "") {
      email.style.border = "solid red";
      validation = false;
    } else {
      email.style.border = "";
    }
    if (message.value == "") {
      message.style.border = "solid red";
      validation = false;
    } else {
      message.style.border = "";
    }
    if (validation) {
      let result = {};
      let response = await sendData(
        { from: email.value, message: message.value },
        "https://mahgpersonalapi.herokuapp.com/mailsender/contact"
      );
      console.log(response);
      if (response.status == 500) {
        result.message = "Ups, my bad please try again later";
        result.color = "red";
      }
      if (response.status == 200) {
        result.message = "I will answer as soon as possible";
        result.color = "green";
      }
      document.getElementById("modal-message").innerHTML = result.message;
      document.getElementById("modal-message").style.color = result.color;
      OpenModal();
    }
  }
  async function sendData(data, url) {
    const response = await fetch(url, {
      method: "POST",
      //cache: 'no-cache',
      // credentials: 'same-origin',
      headers: {
        "Content-Type": "application/json",
      },
      body: JSON.stringify(data),
    });
    return response;
  }
</script>

<form on:submit|preventDefault={validate}>
  <h1>Contact me</h1>
  <input id="email" type="email" placeholder="Email" />
  <textarea
    name=""
    placeholder="Leave a message, suggestion, proposal or just a greeting and I will send you a message!"
    id="message"
    cols="30"
    rows="10"
  />
  <input type="submit" value="Send" />
</form>
<div id="myModal" class="modal">
  <div class="modal-content">
    <i id="close" class="close" on:click={CloseModal}>&times;</i>
    <h1 id="modal-message">Some text in the Modal..</h1>
  </div>
</div>

<style>
  .modal {
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;

    background-color: rgb(0, 0, 0);
    background-color: rgba(0, 0, 0, 0.4);
  }

  .modal-content {
    background-color: #fefefe;
    margin: 7% auto;
    padding: 20px;
    border: 1px solid #888;
    width: 40%;
    height: 21%;
    text-align: center;
  }

  .close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
  }

  .close:hover,
  .close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
  }
  form {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 40vw;
    font-family: "Nunito", sans-serif;
    font-size: 16px;
  }
  form input[type="email"],
  textarea {
    width: calc(100% - 1rem);
    height: 30px;
    margin: 5px;
    font-family: "Nunito";
    font-weight: bold;
  }
  textarea {
    height: 200px;
    font-size: 16px;
    font-family: "Nunito", sans-serif;
  }
  input[type="submit"] {
    background-color: #eeebdd;
    border-radius: 12px;
    display: inline-block;
    cursor: pointer;
    color: #1b1717;
    font-family: "Nunito", sans-serif;
    font-size: 19px;
    padding: 19px 39px;
    text-decoration: none;
  }
  input[type="submit"]:hover {
    background-color: #d6d1ba;
  }
  input[type="submit"]:active {
    background-color: #d6d1ba;
  }

  @media (max-width: 425px) {
    form {
      width: 75vw;
    }
  }
</style>

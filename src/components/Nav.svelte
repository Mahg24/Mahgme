<script>
  export let segment;
  import Fa from "svelte-fa";
  import {
    faBars,
    faTimes,
    faHome,
    faUser,
    faSuitcase,
    faComment,
    faPaperPlane,
  } from "@fortawesome/free-solid-svg-icons";
  let x = false;
  function handleMenu() {
    console.log("?");
    let element = document.querySelector("#menu");
    if (
      element.classList.contains("hide") ||
      !element.classList.contains("show")
    ) {
      element.classList.add("show");
      element.classList.remove("hide");
    } else {
      element.classList.add("hide");
      element.classList.remove("show");
    }
  }
</script>

<div class="icons menu-toggle" id="menu-button">
  <i on:click={handleMenu}><Fa icon={faBars} size="2x" /></i>
</div>
<nav class={x ? "show" : "hide"} id="menu">
  <div class="Nav-Container">
    <div class="icons menu-close">
      <i on:click={handleMenu}><Fa icon={faTimes} size="2x" /></i>
    </div>
    <div class="Nav-Profile">
      <img
        src="https://res.cloudinary.com/mohg24/image/upload/v1620829097/mahgme/assets/Miguel_1_maqclt.jpg"
        alt="Miguel Holguin"
      />
      <div class="Nav-Profile-text">
        <h1>Miguel Holguin</h1>
        <h1>Backend developer</h1>
      </div>
    </div>
    <div class="Nav-Menu">
      <ul>
        <li>
          <div
            class="Menu-button {segment === undefined ? 'active' : undefined}"
          >
            <i>
              <Fa icon={faHome} size="2x" />
            </i>
            <a
              aria-current={segment === undefined ? "page" : undefined}
              href=".">home</a
            >
          </div>
        </li>
        <li>
          <div class="Menu-button {segment === 'about' ? 'active' : undefined}">
            <i>
              <Fa icon={faUser} size="2x" />
            </i>
            <a
              aria-current={segment === "about" ? "page" : undefined}
              href="about">about</a
            >
          </div>
        </li>
        <li>
          <div class="Menu-button {segment === 'holi' ? 'active' : undefined}">
            <i>
              <Fa icon={faSuitcase} size="2x" />
            </i>
            <a
              aria-current={segment === "holi" ? "page" : undefined}
              href="holi">Holi</a
            >
          </div>
        </li>
        <!-- <li>
          <div
            class="Menu-button {segment === 'contact' ? 'active' : undefined}"
          >
            <i>
              <Fa icon={faPaperPlane} size="2x" />
            </i>
            <a
              aria-current={segment === "contact" ? "page" : undefined}
              href="contact">contact</a
            >
          </div>
        </li> -->

        <li>
          <div class="Menu-button {segment === 'blog' ? 'active' : undefined}">
            <i>
              <Fa icon={faComment} size="2x" />
            </i>
            <a
              rel="prefetch"
              aria-current={segment === "blog" ? "page" : undefined}
              href="blog">blog</a
            >
          </div>
        </li>
      </ul>
    </div>
  </div>
</nav>

<style>
  .Menu-button {
    display: flex;
    align-content: center;
    align-items: center;
    height: 45px;
    margin: 15px;
  }
  .Menu-button:hover {
    display: flex;
    align-content: center;
    align-items: center;
    height: 60px;
    font-size: larger;
    font-weight: 900;
    margin: 15px;
  }

  .active {
    height: 60px;
    font-size: larger;
    font-weight: 900;
  }
  .Menu-button a {
    margin-left: 45px;
  }

  ul {
    text-decoration: none;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  ul a {
    font-size: 20px;
    text-decoration: none;
    text-transform: capitalize;
  }
  .Nav-Profile-text {
    text-align: center;
  }
  .menu-toggle {
    position: fixed;
    top: 0px;
  }
  .icons {
    display: none;
  }

  .hide {
    transform: translateX(0vw);
  }
  .show {
    transform: translateX(0vw);
  }
  nav {
    transform: translateX(0vw);
    display: flex;
    transition: transform 1s;
    background-color: #eeebdd;
    height: 100%;
    max-width: 80vw;
    width: 20%;
    min-width: 50px;
    position: fixed;
    top: 0px;
    flex-direction: column;
    align-items: center;
  }
  .Nav-Profile img {
    border-radius: 15px;
    padding-top: 25px;
    width: 215px;
    height: auto;
  }

  @media (max-width: 1440px) {
    nav {
      width: 25%;
    }
  }
  @media (max-width: 768px) {
    .icons i {
      text-align: center;
    }
    .hide {
      transform: translateX(-80vw);
    }

    .icons {
      background-color: #eeebdd;
      width: 50px;
      height: 50px;
      display: flex;
      align-content: center;
      justify-content: center;
      margin: 5px;
      flex-direction: column;
    }
    nav {
      width: 50vw;
    }
  }
  @media (max-width: 425px) {
    nav {
      width: 80vw;
    }
  }
</style>

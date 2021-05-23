<script>
  import Fa from "svelte-fa";
  import { faArrowCircleRight } from "@fortawesome/free-solid-svg-icons";
  export let Name = "Lorem ipsum";
  export let Img =
    "https://res.cloudinary.com/mohg24/image/upload/v1620828760/sample.jpg";
  export let Github = { url: "https://github.com/", private: false };
  export let Url = "http://academy.polygon.us/";
  export let Role = "Backend";
</script>

<div class="Card-Project" style="background-image: url('{Img}');">
  <div class="Card-Project-container">
    <div class="Card-texts">
      <div>
        <div class="Title-Project">
          <h1>{Name}</h1>
        </div>
        <div class="Link-Project">
          <ul>
            {#if !Github.private}
              <li><a href={Github.url}>Github</a></li>
            {/if}
            <li>{Role}</li>
          </ul>
        </div>
      </div>
      <div class="Redirection-project">
        <a target="_blank" href={Url}>
          <i>
            <Fa icon={faArrowCircleRight} size="3x" />
          </i></a
        >
      </div>
    </div>
  </div>
</div>

<style>
  .Card-Project {
    flex: 1 0 33%;
    margin: 30px;
    /* min-width: 421px; */
    min-height: 200px;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 50%;
  }
  .Card-Project-container {
    /* backdrop-filter: blur(2px); */
    height: 100%;
    width: 400px;
  }
  .Card-texts {
    height: 100%;
    width: -webkit-fill-available;
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-direction: row;
    background: linear-gradient(45deg, #584f4f, transparent);
  }
  .Redirection-project {
    width: 20%;
    height: 100%;
    border-left: solid eeebdd 3px;
    display: flex;
    align-content: center;
    justify-content: center;
    align-items: center;
  }
  .Redirection-project a:hover {
    color: #1b1717;
  }
  @media (max-width: 425px) {
    .Card-Project {
      min-width: 100vw;
    }
  }
</style>

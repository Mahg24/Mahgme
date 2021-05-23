<script>
  import { onMount } from "svelte";
  let counter = 0;
  onMount(() => {});
</script>

<svelte:head>
  <title>About</title>
</svelte:head>

<div class="About-Container">
  <h1>Miguel Angel Holguin</h1>
  <div class="About-Resume">
    <div class="About-Resume-text">
      <p>
        My name is Miguel Holguin, i'm a backend developer and a passionate for
        software, i enjoy everything about design, music, games and movies.
      </p>
      <p>I study a lot on the internet and I learned this skills:</p>
      <ul>
        <li>Node js</li>
        <li>Php</li>
        <li>C#</li>
        <li>Svelte</li>
        <li>Adobe Xd</li>
        <li>SQL and Mysql</li>
        <li>Mongo DB</li>
      </ul>
      <p>
        i like the <a href="https://platzi.com/">Platzi</a> slogan "Never stop learning"
        and i live in that way, this are some of skills that I will study or i am
        currently learning
      </p>
      <ul>
        <li>Software architecture</li>
        <li>DevOps</li>
        <li>Laravel</li>
        <li>Graph oriented database</li>
        <li>Movile development</li>
      </ul>
    </div>
    <div class="About-Resume-Image">
      <img
        src="https://res.cloudinary.com/mohg24/image/upload/v1621224043/mahgme/assets/Yothanos_z85z1v.png"
        alt="Mahg Thanos"
      />
    </div>
  </div>
</div>

<style>
  .About-Container {
    text-align: center;
  }
  .About-Resume {
    display: flex;
  }
  .About-Resume-text {
    margin: 0 2vw 0 24vw;
    text-align: justify;
  }

  @media (max-width: 768px) {
    .About-Resume {
      display: flex;
      flex-direction: column;
      flex-direction: column;
      align-items: center;
    }
    .About-Resume-text {
      margin: 0px 14vw 0 14vw !important;
    }
    .About-Resume-Image img {
      width: 90vw;
    }
  }

  @media (max-width: 1440px) {
    .About-Resume-text {
      margin: 0 2vw 0 30vw;
      text-align: justify;
    }
    .About-Resume-Image img {
      width: 400px;
    }
  }
</style>

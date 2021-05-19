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
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad deleniti
        quod facere illo veniam mollitia voluptatibus non laboriosam est,
        accusamus exercitationem id totam similique quidem distinctio
        necessitatibus beatae quae saepe!
      </p>
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

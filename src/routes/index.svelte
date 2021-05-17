<script>
</script>

<svelte:head>
  <title>Miguel Holguin</title>
</svelte:head>
<div class="Ttile-Container">
  <h1>Hi i am Miguel and i am a developer!</h1>
</div>
<figure>
  <img
    alt="Success Kid"
    src="https://res.cloudinary.com/mohg24/image/upload/v1621218179/mahgme/assets/c93d981ab58c4478eb50e1d0ef291edd_uh3elg.gif"
  />
  <figcaption>
    Dancing Shark by Ronan Lynam <a href="http://ronanlynam.tumblr.com"
      >http://ronanlynam.tumblr.com</a
    >
  </figcaption>
</figure>

<style>
  h1,
  figure {
    text-align: center;
    margin: 0 auto;
  }

  h1 {
    font-size: 2.8em;
    /* text-transform: uppercase; */
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  figure {
    margin: 0 0 1em 0;
  }

  img {
    width: 100%;
    max-width: 400px;
    margin: 0 0 2em 0;
  }

  .Ttile-Container {
    width: 40vw;
    margin: auto;
  }
  @media (min-width: 480px) {
    h1 {
      font-size: 3em;
    }
  }

  @media (max-width: 768px) {
    .Ttile-Container {
      width: 100%;
    }
  }
</style>

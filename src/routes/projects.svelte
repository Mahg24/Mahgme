<script>
  import Project from "../components/Projects.svelte";
</script>

<svelte:head>
  <title>Projects</title>
</svelte:head>

<div class="Projects">
  <div class="Projects-container">
    <Project
      Name="Mahgme"
      Url="/"
      Github={{ private: false, url: "https://github.com/Mahg24/Mahgme" }}
      Img="https://res.cloudinary.com/mohg24/image/upload/v1621731131/mahgme/projects/Captura_de_pantalla_2021-05-22_195059_we7j7f.png"
      Role="Backend and Frontend"
    />
    <Project
      Name="Ulumina"
      Url="http://ulumina.co/"
      Github={{ private: true }}
      Img="https://res.cloudinary.com/mohg24/image/upload/v1621731773/mahgme/projects/fondo_h5iwv1.jpg"
      Role="Backend and a little bit of Frontend"
    />
    <Project
      Name="Academy"
      Url="http://academy.polygon.us"
      Github={{ private: true }}
      Img="https://res.cloudinary.com/mohg24/image/upload/v1621732708/mahgme/projects/academy_kyaxvl.png"
      Role="Architecture and Backend"
    />
  </div>
</div>

<style>
  .Projects-container {
    display: flex;
    width: 50%;
    margin-left: 30vw;
    flex-wrap: wrap;
  }
</style>

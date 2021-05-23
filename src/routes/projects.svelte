<script>
  import Project from "../components/Projects.svelte";
</script>

<svelte:head>
  <title>Projects</title>
</svelte:head>

<div class="Projects">
  <div class="Projects-container">
    <Project />
    <Project />
    <Project />
    <Project />
    <Project />
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

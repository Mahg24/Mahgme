<script>
  import { fly } from "svelte/transition";
  export let refresh = "";
</script>

<main class="Main">
  <div class="Main-container">
    {#key refresh}
      <div
        class="Main-content"
        in:fly={{ y: -50, duration: 250, delay: 300 }}
        out:fly={{ y: -50, duration: 250 }}
      >
        <slot />
      </div>
    {/key}
  </div>
</main>

<style>
  main {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 10vh;
    color: #eeebdd;
  }
  /* .Main-container {
  }
  .Main-content {
  } */
</style>

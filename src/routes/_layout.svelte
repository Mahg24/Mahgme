<script>
  import Nav from "../components/Nav.svelte";
  import Main from "../components/Main.svelte";
  export let segment;
</script>

<Nav {segment} />

<Main refresh={segment}>
  <slot />
</Main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200;0,300;0,400;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,600;1,700;1,900&display=swap");
  :global(html) {
    background-color: #1b1717;
  }
  :global(body) {
    font-family: "Nunito", sans-serif;
  }
</style>

<script>
  import "./styles.css";
  import Header from "../components/Header.svelte";
</script>

<div class="app">
  <main>
    <slot />
  </main>

  <footer />
</div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Abyssinica+SIL&display=swap");
  .app {
    font-family: "Abyssinica SIL", serif;
  }
</style>

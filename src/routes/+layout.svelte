<script>
  import './styles.css';
  import NavBar from '../components/NavBar.svelte';
</script>

<div class="app">
  <NavBar />
  <main>
    <slot />
  </main>

  <footer />
</div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Abyssinica+SIL&display=swap');
  .app {
    font-family: 'Abyssinica SIL', serif;
  }
</style>

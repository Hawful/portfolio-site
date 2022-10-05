<script>
  import "./styles.css";
  import Header from "./Header.svelte";
</script>

<Header />
<div class="app">
  <main>
    <slot />
  </main>

  <footer>
    <p>stay chill and cool</p>
  </footer>
</div>

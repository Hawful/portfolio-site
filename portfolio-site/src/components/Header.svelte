<script>
  import { page } from "$app/stores";
</script>

<header>
  <nav>
    <ul>
      <li class:active={$page.url.pathname === "/"}>
        <a href="/">Home</a>
      </li>
      <li class:active={$page.url.pathname === "/about"}>
        <a href="/about">About</a>
      </li>
      <li class:active={$page.url.pathname === "/blog"}>
        <a href="/blog">Blog</a>
      </li>
      <li class:active={$page.url.pathname === "/projects"}>
        <a href="/projects">Projects</a>
      </li>
      <li class:active={$page.url.pathname === "/contact"}>
        <a href="/contact">Contact</a>
      </li>
    </ul>
  </nav>
</header>

<style>
  header {
    display: flex;
    justify-content: space-between;
  }

  nav {
    display: flex;
    flex-direction: row-reverse;
    justify-content: center;
    --background: rgba(255, 255, 255, 0.7);
  }

  ul {
    position: relative;
    padding: 0;
    margin: 0;
    height: 3em;
    display: flex;
    justify-content: center;
    align-items: center;
    list-style: none;
    background: var(--background);
    background-size: contain;
  }

  li {
    position: relative;
    height: 100%;
  }

  nav a {
    display: flex;
    height: 100%;
    align-items: center;
    padding: 0 0.5rem;
    color: var(--color-text);
    font-weight: 700;
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    text-decoration: none;
    transition: color 0.2s linear;
  }

  a:hover {
    color: red;
  }
</style>

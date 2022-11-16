<script>
  import { page } from '$app/stores';
</script>

<header>
  <nav>
    <ul>
      <li class:active={$page.url.pathname === '/'}>
        <a href="/">Home</a>
      </li>
      <li class:active={$page.url.pathname === '/about'}>
        <a href="/about">About</a>
      </li>
      <li class:active={$page.url.pathname === '/blog'}>
        <a href="/blog">Blog</a>
      </li>
      <li class:active={$page.url.pathname === '/projects'}>
        <a href="/projects">Projects</a>
      </li>
      <li class:active={$page.url.pathname === '/contact'}>
        <a href="/contact">Contact</a>
      </li>
    </ul>
  </nav>
  <div />
</header>

<style type="scss">
  header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    z-index: 15;
    div {
      width: 100%;
      height: 3rem;
      background: linear-gradient(#f2f2e7, #f2f2e700);
    }
  }

  nav {
    background-color: #f2f2e7;
    display: flex;
    justify-content: space-around;
    color: inherit;
  }

  ul {
    position: relative;
    padding: 0;
    margin: 0;
    height: 3em;
    display: flex;
    justify-content: space-between;
    list-style: none;
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
    font-weight: 700;
    font-size: 0.8rem;
    color: inherit;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    text-decoration: none;
    transition: color 0.2s linear;
  }

  a:hover {
    color: black;
  }
</style>

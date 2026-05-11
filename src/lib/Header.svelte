<script>
  let { logo = "tuxterm@portfolio:~$" } = $props();
</script>

<header>
  <div class="logo">
    <a href="#/">{logo}</a>
  </div>
  <nav>
    <ul>
      <li><a href="#/">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#/blog">Blog</a></li>
    </ul>
  </nav>
</header>

<style>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 3rem 0;
    margin-bottom: 2rem;
  }

  .logo a {
    color: var(--fg);
    font-weight: 700;
    text-decoration: none;
    border: none;
    font-size: 1.1rem;
  }

  .logo a:hover {
    color: var(--accent);
    background: transparent;
  }

  nav ul {
    list-style: none;
    display: flex;
    gap: 1.5rem;
    margin: 0;
    padding: 0;
  }

  nav a {
    text-decoration: none;
    border: none;
    color: var(--fg);
    font-size: 1rem;
  }

  nav a:hover {
    color: var(--bg);
    background-color: var(--accent);
  }

  @media (max-width: 600px) {
    header {
      flex-direction: column;
      align-items: flex-start;
      gap: 1rem;
    }
  }
</style>

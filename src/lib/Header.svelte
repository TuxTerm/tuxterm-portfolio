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
      <li><a href="#/tools">Tools</a></li>
      <li><a href="#/blog">Blog</a></li>
    </ul>
  </nav>
</header>

<style>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 3rem 2rem;
    margin-bottom: 2rem;
    width: 100%;
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
    flex-wrap: wrap;
    gap: 1.5rem;
    margin: 0;
    padding: 0;
  }

  nav a {
    position: relative;
    display: inline-block;
    text-decoration: none;
    border: none;
    color: var(--fg);
    font-size: 1rem;
    padding: 0.1rem 0.3rem;
    z-index: 1;
    transition: color 0.3s ease;
  }

  nav a::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    background-color: var(--accent);
    z-index: -1;
    transition: width 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  }

  nav a:hover {
    color: var(--bg);
    transition-delay: 0.1s;
  }

  nav a:hover::before {
    width: 100%;
  }

  @media (max-width: 768px) {
    header {
      flex-direction: column;
      align-items: flex-start;
      padding: 2rem 1.5rem;
      gap: 1.5rem;
    }

    nav ul {
      gap: 1rem 1.2rem;
    }
  }
</style>

<script>
  import { onMount } from 'svelte';

  let dotCount = $state(0);

  onMount(() => {
    const interval = setInterval(() => {
      dotCount = (dotCount + 1) % 4;
    }, 500);

    return () => clearInterval(interval);
  });

  const getDots = () => '.'.repeat(dotCount);
</script>

<section id="home" class="coming-soon">
  <div class="container">
    <div class="content">
      <h1 class="title">
        <span class="terminal-prefix">tuxterm@portfolio:~$</span>
        <span class="command">portfolio init</span>
      </h1>

      <div class="loading-animation">
        <div class="spinner"></div>
        <p class="loading-text">Initializing portfolio{getDots()}</p>
      </div>

      <div class="message">
        <p class="coming-soon-text">
          Something amazing is coming soon. While we prepare, explore my work and projects.
        </p>
      </div>

      <div class="quick-links">
        <h2>Quick Navigation</h2>
        <div class="links-grid">
          <a href="#/about" class="link-card">
            <span class="icon">👤</span>
            <span class="label">About Me</span>
          </a>
          <a href="#/blog" class="link-card">
            <span class="icon">📝</span>
            <span class="label">Blog & Write-ups</span>
          </a>
          <a href="#/tools" class="link-card">
            <span class="icon">🛠️</span>
            <span class="label">Tools & Setup</span>
          </a>
          <a href="https://github.com/TuxTerm" target="_blank" rel="noopener noreferrer" class="link-card">
            <span class="icon">🐙</span>
            <span class="label">GitHub Profile</span>
          </a>
        </div>
      </div>

      <div class="footer-message">
        <p>In the meantime, check out my <a href="#/about">portfolio</a> or <a href="#/blog">latest articles</a>.</p>
      </div>
    </div>
  </div>
</section>

<style>
  #home {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 2rem;
  }

  .container {
    max-width: 800px;
    width: 100%;
  }

  .content {
    text-align: center;
    animation: fadeIn 0.8s ease-out;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .title {
    font-size: 1.8rem;
    margin-bottom: 3rem;
    font-family: 'Fira Code', monospace;
    font-weight: 700;
    letter-spacing: 0.05em;
  }

  .terminal-prefix {
    color: var(--fg-secondary);
    display: block;
    margin-bottom: 0.5rem;
    font-size: 1rem;
  }

  .command {
    color: var(--accent);
    display: block;
  }

  .loading-animation {
    margin: 3rem 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }

  .spinner {
    width: 50px;
    height: 50px;
    border: 3px solid var(--border);
    border-top: 3px solid var(--accent);
    border-radius: 50%;
    animation: spin 1s linear infinite;
  }

  @keyframes spin {
    to {
      transform: rotate(360deg);
    }
  }

  .loading-text {
    color: var(--fg);
    font-size: 1.1rem;
    font-family: 'Fira Code', monospace;
    font-weight: 500;
    min-width: 200px;
    text-align: center;
  }

  .message {
    margin: 2rem 0;
  }

  .coming-soon-text {
    color: var(--fg);
    font-size: 1.1rem;
    line-height: 1.8;
    margin-bottom: 2rem;
  }

  .quick-links {
    margin: 3rem 0;
  }

  .quick-links h2 {
    font-size: 1.3rem;
    margin-bottom: 1.5rem;
    color: var(--fg);
    position: relative;
    display: inline-block;
    z-index: 1;
    padding: 0.1rem 0.3rem;
    margin-left: -0.3rem;
    transition: color 0.3s ease;
  }

  .quick-links h2::after {
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

  .quick-links:hover h2 {
    color: var(--bg);
    transition-delay: 0.1s;
  }

  .quick-links:hover h2::before {
    color: var(--bg);
    transition-delay: 0.1s;
  }

  .quick-links:hover h2::after {
    width: 100%;
  }

  .links-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 1rem;
    margin-bottom: 2rem;
  }

  .link-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 0.75rem;
    padding: 1.5rem;
    background-color: var(--bg);
    border: 2px solid var(--border);
    border-radius: 8px;
    text-decoration: none;
    color: var(--fg);
    transition: all 0.3s ease;
  }

  .link-card:hover {
    border-color: var(--accent);
    background-color: rgba(242, 162, 114, 0.1);
    transform: translateY(-4px);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  }

  .link-card:focus-visible {
    outline: 2px solid var(--accent);
    outline-offset: 2px;
  }

  .icon {
    font-size: 2rem;
  }

  .label {
    font-size: 0.9rem;
    font-weight: 500;
    text-align: center;
    color: var(--accent);
  }

  .footer-message {
    margin-top: 2rem;
    padding-top: 2rem;
    border-top: 1px dashed var(--border);
  }

  .footer-message p {
    color: var(--fg-secondary);
    font-size: 0.95rem;
  }

  .footer-message a {
    color: var(--accent);
    text-decoration: none;
    border-bottom: 1px solid var(--accent);
    transition: all 0.3s ease;
  }

  .footer-message a:hover {
    background-color: var(--accent);
    color: var(--bg);
  }

  @media (max-width: 768px) {
    #home {
      min-height: auto;
      padding: 2rem 1rem;
    }

    .title {
      font-size: 1.3rem;
      margin-bottom: 2rem;
    }

    .terminal-prefix {
      font-size: 0.85rem;
    }

    .links-grid {
      grid-template-columns: repeat(2, 1fr);
      gap: 0.75rem;
    }

    .link-card {
      padding: 1rem;
    }

    .icon {
      font-size: 1.5rem;
    }

    .label {
      font-size: 0.8rem;
    }
  }
</style>

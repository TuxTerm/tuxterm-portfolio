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
          <a href="#/about" class="link-card" title="About Me">
            <svg class="icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle cx="9" cy="9" r="2" stroke="currentColor" stroke-width="1.5"/>
              <path d="M13 15C13 16.1046 13 17 9 17C5 17 5 16.1046 5 15C5 13.8954 6.79086 13 9 13C11.2091 13 13 13.8954 13 15Z" stroke="currentColor" stroke-width="1.5"/>
              <path d="M2 12C2 8.22876 2 6.34315 3.17157 5.17157C4.34315 4 6.22876 4 10 4H14C17.7712 4 19.6569 4 20.8284 5.17157C22 6.34315 22 8.22876 22 12C22 15.7712 22 17.6569 20.8284 18.8284C19.6569 20 17.7712 20 14 20H10C6.22876 20 4.34315 20 3.17157 18.8284C2 17.6569 2 15.7712 2 12Z" stroke="currentColor" stroke-width="1.5"/>
              <path d="M19 12H15" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
              <path d="M19 9H14" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
              <path d="M19 15H16" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
            </svg>
            <span class="label">About Me</span>
          </a>
          <a href="#/blog" class="link-card" title="Blog & Write-ups">
            <svg class="icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M4 8C4 5.17157 4 3.75736 4.87868 2.87868C5.75736 2 7.17157 2 10 2H14C16.8284 2 18.2426 2 19.1213 2.87868C20 3.75736 20 5.17157 20 8V16C20 18.8284 20 20.2426 19.1213 21.1213C18.2426 22 16.8284 22 14 22H10C7.17157 22 5.75736 22 4.87868 21.1213C4 20.2426 4 18.8284 4 16V8Z" stroke="currentColor" stroke-width="1.5"/>
              <path d="M19.8978 16H7.89778C6.96781 16 6.50282 16 6.12132 16.1022C5.08604 16.3796 4.2774 17.1883 4 18.2235" stroke="currentColor" stroke-width="1.5"/>
              <path d="M8 7H16" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
              <path d="M8 10.5H13" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
              <path d="M13 16V19.5309C13 19.8065 13 19.9443 12.9051 20C12.8103 20.0557 12.6806 19.9941 12.4211 19.8708L11.1789 19.2808C11.0911 19.2391 11.0472 19.2182 11 19.2182C10.9528 19.2182 10.9089 19.2391 10.8211 19.2808L9.57889 19.8708C9.31943 19.9941 9.18971 20.0557 9.09485 20C9 19.9443 9 19.8065 9 19.5309V16.45" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
            </svg>
            <span class="label">Blog & Write-ups</span>
          </a>
          <a href="#/tools" class="link-card" title="Tools & Setup">
            <svg class="icon" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" fill="currentColor">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M14.773 3.485l-.78-.184-2.108 2.096-1.194-1.216 2.056-2.157-.18-.792a4.42 4.42 0 0 0-1.347-.228 3.64 3.64 0 0 0-1.457.28 3.824 3.824 0 0 0-1.186.84 3.736 3.736 0 0 0-.875 1.265 3.938 3.938 0 0 0 0 2.966 335.341 335.341 0 0 0-6.173 6.234c-.21.275-.31.618-.284.963a1.403 1.403 0 0 0 .464.967c.124.135.272.247.437.328.17.075.353.118.538.127.316-.006.619-.126.854-.337 1.548-1.457 4.514-4.45 6.199-6.204.457.194.948.294 1.444.293a3.736 3.736 0 0 0 2.677-1.133 3.885 3.885 0 0 0 1.111-2.73 4.211 4.211 0 0 0-.196-1.378zM2.933 13.928a.31.31 0 0 1-.135.07.437.437 0 0 1-.149 0 .346.346 0 0 1-.144-.057.336.336 0 0 1-.114-.11c-.14-.143-.271-.415-.14-.568 1.37-1.457 4.191-4.305 5.955-6.046.1.132.21.258.328.376.118.123.245.237.38.341-1.706 1.75-4.488 4.564-5.98 5.994zm11.118-9.065c.002.765-.296 1.5-.832 2.048a2.861 2.861 0 0 1-4.007 0 2.992 2.992 0 0 1-.635-3.137A2.748 2.748 0 0 1 10.14 2.18a2.76 2.76 0 0 1 1.072-.214h.254L9.649 3.839v.696l1.895 1.886h.66l1.847-1.816v.258zM3.24 6.688h1.531l.705.717.678-.674-.665-.678V6.01l.057-1.649-.22-.437-2.86-1.882-.591.066-.831.849-.066.599 1.838 2.918.424.215zm-.945-3.632L4.609 4.58 4.57 5.703H3.494L2.002 3.341l.293-.285zm7.105 6.96l.674-.673 3.106 3.185a1.479 1.479 0 0 1 0 2.039 1.404 1.404 0 0 1-1.549.315 1.31 1.31 0 0 1-.437-.315l-3.142-3.203.679-.678 3.132 3.194a.402.402 0 0 0 .153.105.477.477 0 0 0 .359 0 .403.403 0 0 0 .153-.105.436.436 0 0 0 .1-.153.525.525 0 0 0 .036-.184.547.547 0 0 0-.035-.184.436.436 0 0 0-.1-.153L9.4 10.016z"/>
            </svg>
            <span class="label">Tools & Setup</span>
          </a>
          <a href="https://github.com/TuxTerm" target="_blank" rel="noopener noreferrer" class="link-card" title="GitHub Profile">
            <svg class="icon" viewBox="0 0 192 192" xmlns="http://www.w3.org/2000/svg" fill="none"><path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="12" d="M120.755 170c.03-4.669.059-20.874.059-27.29 0-9.272-3.167-15.339-6.719-18.41 22.051-2.464 45.201-10.863 45.201-49.067 0-10.855-3.824-19.735-10.175-26.683 1.017-2.516 4.413-12.63-.987-26.32 0 0-8.296-2.672-27.202 10.204-7.912-2.213-16.371-3.308-24.784-3.352-8.414.044-16.872 1.14-24.785 3.352C52.457 19.558 44.162 22.23 44.162 22.23c-5.4 13.69-2.004 23.804-.987 26.32C36.824 55.498 33 64.378 33 75.233c0 38.204 23.149 46.603 45.2 49.067-3.551 3.071-6.719 9.138-6.719 18.41 0 6.416.03 22.621.059 27.29M27 130c9.939.703 15.67 9.735 15.67 9.735 8.834 15.199 23.178 10.803 28.815 8.265"/></svg>
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

  .quick-links h2::before {
    content: "[+] ";
    color: var(--accent);
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
    border-radius: 0;
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
    width: 32px;
    height: 32px;
    color: var(--accent);
    transition: all 0.3s ease;
  }

  .link-card:hover .icon {
    color: var(--accent);
    transform: scale(1.1);
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

<section id="tools">
  <h2>Tools & System Config</h2>
  <p>Here is a detailed breakdown of the applications, configurations, and tools I use on a daily basis for my Linux system.</p>
  
  <div class="tool-category">
    <h3>OS & Environment</h3>
    <ul>
      <li><strong>OS:</strong> Linux (Custom configured)</li>
      <li><strong>Terminal:</strong> Kitty</li>
      <li><strong>Shell:</strong> NuShell / Bash</li>
      <li><strong>Theme:</strong> BubbleGum</li>
    </ul>
  </div>

  <div class="tool-category">
    <h3>Development & Editors</h3>
    <ul>
      <li><strong>Editors:</strong> VS Code, Zed, Neovim</li>
      <li><strong>Version Control:</strong> Git, Lazy Git</li>
      <li><strong>Containerization:</strong> Docker, Lazy Docker</li>
    </ul>
  </div>

  <div class="tool-category">
    <h3>Security & Networking</h3>
    <ul>
      <li><strong>Traffic Analysis:</strong> Wireshark, TCPdump</li>
      <li><strong>Testing & Exploitation:</strong> Nmap, Burp Suite, Metasploit</li>
      <li><strong>Reverse Engineering:</strong> Ghidra SRE, CyberChef</li>
    </ul>
  </div>
</section>

<style>
  .tool-category {
    margin-top: 2rem;
  }
  
  .tool-category h3 {
    margin-bottom: 0.5rem;
    color: var(--accent);
  }

  .tool-category h3::before {
    content: ">> ";
  }

  ul {
    list-style-type: none;
    padding-left: 1rem;
  }

  li {
    margin-bottom: 0.8rem;
    position: relative;
  }

  li::before {
    content: "- ";
    color: var(--border);
    position: absolute;
    left: -1rem;
  }
</style>

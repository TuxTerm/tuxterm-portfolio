<script>
  import { posts } from '../data/posts.js';
</script>

<section id="blog">
  <h2>Blog & Write-ups</h2>
  <p>Recent progress, CTF write-ups, and cybersecurity thoughts.</p>
  
  <div class="posts">
    {#each posts as post}
      <article class="post">
        <h3><a href={post.link}>{post.title}</a></h3>
        <div class="meta">{post.date}</div>
        <p>{post.summary}</p>
      </article>
    {/each}
  </div>
</section>

<style>
  .posts {
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    margin-top: 2rem;
  }
  
  .post h3 {
    margin-bottom: 0.5rem;
  }
  
  .post h3::before {
    content: ">> ";
    color: var(--accent);
  }
  
  .meta {
    font-size: 0.9rem;
    color: var(--border);
    margin-bottom: 1rem;
  }
</style>
<script>
  import { onMount } from 'svelte';
  import { fade } from 'svelte/transition';
  import Header from './lib/Header.svelte';
  import Hero from './lib/Hero.svelte';
  import Experience from './lib/Experience.svelte';
  import Skills from './lib/Skills.svelte';
  import Projects from './lib/Projects.svelte';
  import Contact from './lib/Contact.svelte';
  import Blog from './lib/Blog.svelte';

  let currentHash = $state('');

  onMount(() => {
    currentHash = window.location.hash;
    const handleHashChange = () => {
      currentHash = window.location.hash;
    };
    window.addEventListener('hashchange', handleHashChange);
    return () => window.removeEventListener('hashchange', handleHashChange);
  });

  let isBlog = $derived(currentHash === '#/blog');
</script>

<div class="container">
  <Header />
  {#key isBlog}
    <main in:fade={{ duration: 300 }}>
      {#if isBlog}
        <Blog />
      {:else}
        <Hero />
        <Experience />
        <Skills />
        <Projects />
        <Contact />
      {/if}
    </main>
  {/key}
</div>

<style>
</style>
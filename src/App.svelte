<script>
  import { onMount } from 'svelte';
  import { fade } from 'svelte/transition';
  import Header from './lib/Header.svelte';
  import Home from './lib/Home.svelte';
  import About from './lib/About.svelte';
  import Blog from './lib/Blog.svelte';
  import Tools from './lib/Tools.svelte';

  let currentHash = $state('');

  onMount(() => {
    currentHash = window.location.hash;
    const handleHashChange = () => {
      currentHash = window.location.hash;
    };
    window.addEventListener('hashchange', handleHashChange);
    return () => window.removeEventListener('hashchange', handleHashChange);
  });

  let isHome = $derived(currentHash === '#/' || currentHash === '');
  let isAbout = $derived(currentHash === '#/about');
  let isBlog = $derived(currentHash === '#/blog');
  let isTools = $derived(currentHash === '#/tools');
  let currentView = $derived(currentHash);
</script>

<Header />
<div class="container">
  {#key currentView}
    <main in:fade={{ duration: 300 }}>
      {#if isHome}
        <Home />
      {:else if isAbout}
        <About />
      {:else if isBlog}
        <Blog />
      {:else if isTools}
        <Tools />
      {:else}
        <Home />
      {/if}
    </main>
  {/key}
</div>

<style>
</style>
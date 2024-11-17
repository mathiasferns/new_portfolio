<script>
  import Header from './lib/components/Header.svelte';
  import Hero from './lib/components/Hero.svelte';
  import Skills from './lib/components/Skills.svelte';
  import Projects from './lib/components/Projects.svelte';
  import Contact from './lib/components/Contact.svelte';
</script>

<div class="animated-bg"></div>
<main class="relative">
  <Header />
  <Hero />
  <Skills />
  <Projects />
  <Contact />
</main>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }
</style>
<script>
  import { onMount } from 'svelte';
  let typed = '';
  const fullText = 'An engineer with a fun journey ahead';
  
  onMount(() => {
    let i = 0;
    const interval = setInterval(() => {
      typed = fullText.substring(0, i);
      i++;
      if (i > fullText.length) clearInterval(interval);
    }, 100);
  });
</script>

<section id="home" class="min-h-screen flex items-center justify-center">
  <div class="text-center px-6 py-12 backdrop-blur-md bg-white/30 rounded-2xl shadow-lg max-w-3xl mx-4">
    <h1 class="text-5xl md:text-6xl font-bold mb-4 text-gray-900">Mathias Fernandes</h1>
    <p class="text-xl md:text-2xl text-gray-800 mb-8">{typed}_</p>
    <div class="flex flex-col sm:flex-row justify-center gap-4">
      <a href="#projects" class="bg-white/80 hover:bg-white text-gray-900 px-6 py-3 rounded-lg transition duration-300 shadow-md hover:shadow-lg">
        View Projects
      </a>
      <a href="#contact" class="bg-black/80 hover:bg-black text-white px-6 py-3 rounded-lg transition duration-300 shadow-md hover:shadow-lg">
        Contact Me
      </a>
    </div>
  </div>
</section>
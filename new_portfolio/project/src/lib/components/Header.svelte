<script>
  let isMenuOpen = false;
  const toggleMenu = () => isMenuOpen = !isMenuOpen;
</script>

<header class="fixed w-full bg-white/90 backdrop-blur-sm shadow-sm z-50">
  <nav class="container mx-auto px-6 py-4">
    <div class="flex justify-between items-center">
      <a href="#home" class="text-2xl font-bold text-gray-800">Mathias Fernandes</a>
      
      <button class="md:hidden" on:click={toggleMenu}>
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d={isMenuOpen ? "M6 18L18 6M6 6l12 12" : "M4 6h16M4 12h16M4 18h16"}/>
        </svg>
      </button>

      <div class="hidden md:flex space-x-8">
        <a href="#about" class="text-gray-600 hover:text-gray-900">About</a>
        <a href="#skills" class="text-gray-600 hover:text-gray-900">Skills</a>
        <a href="#projects" class="text-gray-600 hover:text-gray-900">Projects</a>
        <a href="#contact" class="text-gray-600 hover:text-gray-900">Contact</a>
      </div>
    </div>

    {#if isMenuOpen}
      <div class="md:hidden mt-4 space-y-4">
        <a href="#about" class="block text-gray-600 hover:text-gray-900">About</a>
        <a href="#skills" class="block text-gray-600 hover:text-gray-900">Skills</a>
        <a href="#projects" class="block text-gray-600 hover:text-gray-900">Projects</a>
        <a href="#contact" class="block text-gray-600 hover:text-gray-900">Contact</a>
      </div>
    {/if}
  </nav>
</header>
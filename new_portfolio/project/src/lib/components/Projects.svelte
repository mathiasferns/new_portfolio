<script>
  const projects = [
    {
      title: 'Based GPT',
      description: 'An advanced GPT-based solution for natural language processing and generation.',
      tech: ['AI/ML', 'NLP', 'Python'],
    },
    {
      title: 'Crime Management Software',
      description: 'Comprehensive system for law enforcement to manage and analyze crime data.',
      tech: ['Database', 'Security', 'Analytics'],
    },
    {
      title: 'Radical Content Detection',
      description: 'AI-powered system to identify and flag radical content across digital platforms.',
      tech: ['Machine Learning', 'Content Analysis', 'Security'],
    }
  ];
</script>

<section id="projects" class="py-20">
  <div class="container mx-auto px-6">
    <h2 class="text-3xl font-bold text-center mb-12 text-gray-900">Featured Projects</h2>
    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each projects as project}
        <div class="backdrop-blur-md bg-white/30 rounded-2xl shadow-lg p-8 hover:shadow-xl transition duration-300">
          <h3 class="text-xl font-semibold mb-3 text-gray-900">{project.title}</h3>
          <p class="text-gray-800 mb-4">{project.description}</p>
          <div class="flex flex-wrap gap-2">
            {#each project.tech as tech}
              <span class="bg-black/10 backdrop-blur-sm text-gray-900 text-sm px-3 py-1 rounded-full">{tech}</span>
            {/each}
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
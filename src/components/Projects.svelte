<script>
  let projects = [
    {
      title: 'Portfolio Website',
      description: 'A personal site built with Svelte + Tailwind.',
      skills: ['Svelte', 'Tailwind CSS', 'Vite'],
      live: 'https://yourportfolio.live',
      repo: 'https://github.com/yourusername/portfolio'
    },
    {
      title: 'Geo Trumps',
      description: 'A Top trumps inspired game created from a brief asking us to make an educational game for a school.',
      skills: ['Javascript', 'HTML', 'CSS', 'Node.js'],
      // live not provided
      repo: 'https://github.com/yourusername/fakestore'
    }
  ];
</script>

<section id="projects" class="py-20 px-4 bg-gray-200 text-center">
  <h2 class="text-3xl font-bold mb-10">Projects</h2>
  <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
    {#each projects as project}
      <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition text-left">
        <h3 class="text-xl font-semibold mb-2">{project.title}</h3>
        <p class="text-gray-700 mb-3">{project.description}</p>
        
        {#if project.skills}
          <div class="flex flex-wrap gap-2 mb-4">
            {#each project.skills as skill}
              <span class="bg-gray-300 text-sm text-gray-800 px-2 py-1 rounded-full">{skill}</span>
            {/each}
          </div>
        {/if}

        <div class="flex gap-4 mt-4">
          {#if project.live}
            <a href={project.live} target="_blank" class="text-blue-600 font-semibold hover:underline">
              Live Site →
            </a>
          {/if}
          {#if project.repo}
            <a href={project.repo} target="_blank" class="text-gray-700 font-semibold hover:underline">
              GitHub →
            </a>
          {/if}
        </div>
      </div>
    {/each}
  </div>
</section>

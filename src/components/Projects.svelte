<script>
let projects = [
  {
    title: 'Geo Trumps',
    description: 'A Top Trumps-inspired educational game designed to help students learn about countries. Players select attributes to compete against a CPU card, encouraging geographical knowledge. Includes a leaderboard to promote healthy competition.',
    skills: ['HTML', 'CSS', 'JavaScript', 'Node.js'],
    frontend: 'https://geo-trumps.onrender.com/',
    frontendRepo: 'https://github.com/kenenx/Geo_Trumps_FE',
    backend: 'https://geo-trumps-api.onrender.com/',
    backendRepo: 'https://github.com/kenenx/Geo_Trumps_BE'
  },
  {
    title: 'Florin Country Council',
    description: 'A community website allowing members and businesses in Florin County to interact using only HTML, CSS, JavaScript, and Bootstrap. Backend service no longer active, but frontend demo remains available.',
    skills: ['HTML', 'CSS', 'JavaScript', 'Bootstrap', 'Node.js', 'SQL', 'Jest', 'Express', 'Supertest'],
    frontend: 'https://florin-county-council-client.onrender.com/',
    frontendRepo: 'https://github.com/CingSharped/florin-client',
    backend: 'https://florin-server-web.onrender.com/',
    backendRepo: 'https://github.com/CingSharped/florin_server'
  },
  {
    title: 'Crammerdoro',
    description: 'A fullstack flashcard and quiz app with an integrated pomodoro timer. Users can study various subjects and track their scores, which are saved in a MongoDB database.',
    skills: ['Vite', 'React', 'Bootstrap', 'Vitest', 'Jest', 'Express', 'Mongoose', 'MongoDB'],
    frontend: 'https://crammerdoro.onrender.com/',
    frontendRepo: 'https://github.com/CingSharped/crammerdoro/tree/staging/frontend',
    backend: 'https://crammerdoro-backend.onrender.com/',
    backendRepo: 'https://github.com/CingSharped/crammerdoro/tree/staging/backend'
  },
  {
    title: 'Propertease',
    description: 'A fullstack property management app with 3D IFC/BIM integration using IFC.js. Landlords, tenants, and service workers manage properties and maintenance linked to specific elements in the 3D model. Helps monitor profits and streamlines maintenance.',
    skills: ['Vite', 'React', 'Vitest', 'Jest', 'Express', 'Mongoose', 'MongoDB', 'ChartJS'],
    frontendRepo: 'https://github.com/CingSharped/propertease/tree/staging/frontend',
    backendRepo: 'https://github.com/CingSharped/propertease/tree/staging/backend'
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
              <span class="bg-red-300 text-sm text-gray-800 px-2 py-1 rounded-full">{skill}</span>
            {/each}
          </div>
        {/if}
        <div class="flex gap-4 mt-4">
          <div class="flex flex-col gap-2 mt-4 text-sm">
            {#if project.frontend}
              <a href={project.frontend} target="_blank" class="text-blue-600 font-semibold hover:underline">
                🌐 Frontend Live →
              </a>
            {/if}
            {#if project.frontendRepo}
              <a href={project.frontendRepo} target="_blank" class="text-gray-700 hover:underline">
                🗂️ Frontend Repo →
              </a>
            {/if}
            {#if project.backend}
              <a href={project.backend} target="_blank" class="text-blue-600 font-semibold hover:underline">
                🛠️ Backend Live →
              </a>
            {/if}
            {#if project.backendRepo}
              <a href={project.backendRepo} target="_blank" class="text-gray-700 hover:underline">
                💾 Backend Repo →
              </a>
            {/if}
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>

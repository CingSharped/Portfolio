<script>
  import Hero from './components/Hero.svelte';
  import About from './components/About.svelte';
  import Projects from './components/Projects.svelte';
  import Contact from './components/Contact.svelte';

  let dark = false;

  function toggleDark() {
    dark = !dark;
    const html = document.documentElement;
    html.classList.toggle('dark', dark);
  }
</script>

<main class="min-h-screen bg-base text-highlight dark:bg-highlight dark:text-black transition-colors duration-300">

  <Hero />
  <About />
  <Projects />
  <!-- <Contact /> -->
</main>

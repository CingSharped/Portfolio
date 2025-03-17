<script>
  let name = '';
  let email = '';
  let message = '';
</script>

<section class="py-20 px-4 bg-white text-center">
  <h2 class="text-3xl font-bold mb-6">Contact Me</h2>
  <form class="max-w-xl mx-auto space-y-4">
    <input class="w-full p-3 border rounded" type="text" placeholder="Your Name" bind:value={name} />
    <input class="w-full p-3 border rounded" type="email" placeholder="Your Email" bind:value={email} />
    <textarea class="w-full p-3 border rounded" rows="5" placeholder="Your Message" bind:value={message}></textarea>
    <button class="mt-8 px-8 py-4 bg-red-600 text-white font-semibold rounded-full shadow-md hover:shadow-lg hover:bg-red-700 transition-all duration-300 ease-in-out">Send Message</button>
  </form>
</section>

<script>
  let name = "";
  let email = "";
  let message = "";
  let submitted = false;

  function submitForm() {
    submitted = true; 
  }
</script>

<section class="py-12 lg:py-20 flex flex-col items-center gap-10 text-center">
  {#if !submitted}
    <div class="flex flex-col gap-2">
      <h6 class="text-lg sm:text-xl md:text-2xl">Get in Touch</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Let's <span class="poppins text-violet-400">Connect</span>
      </h3>
    </div>

    <form on:submit|preventDefault={submitForm} class="max-w-lg w-full bg-gray-900 p-6 rounded-lg shadow-lg">
      <div class="mb-4">
        <label for="name" class="block text-left text-gray-300 mb-2">Name</label>
        <input type="text" id="name" bind:value={name} class="w-full px-4 py-2 rounded-md bg-gray-800 text-white border border-gray-700 focus:border-violet-500 focus:ring-violet-500 outline-none" required />
      </div>

      <div class="mb-4">
        <label for="email" class="block text-left text-gray-300 mb-2">Email</label>
        <input type="email" id="email" bind:value={email} class="w-full px-4 py-2 rounded-md bg-gray-800 text-white border border-gray-700 focus:border-violet-500 focus:ring-violet-500 outline-none" required />
      </div>

      <div class="mb-4">
        <label for="message" class="block text-left text-gray-300 mb-2">Message</label>
        <textarea id="message" bind:value={message} rows="4" class="w-full px-4 py-2 rounded-md bg-gray-800 text-white border border-gray-700 focus:border-violet-500 focus:ring-violet-500 outline-none" required></textarea>
      </div>

      <button type="submit" class="w-full px-6 py-3 bg-violet-600 text-white rounded-md hover:bg-violet-700 transition duration-200">
        Send Message
      </button>
    </form>
  {:else}
    <div class="flex flex-col gap-2">
      <h6 class="text-lg sm:text-xl md:text-2xl">Thank you for</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        <span class="poppins text-violet-400">Connecting</span>
      </h3>
    </div>
  {/if}

  <div class="flex gap-6 text-xl text-white">
    <a href="https://facebook.com" class="!text-white hover:text-violet-500 transition"><i class="fa-brands fa-facebook"></i></a>
    <a href="https://twitter.com" class="!text-white hover:text-violet-500 transition"><i class="fa-brands fa-x-twitter"></i></a>
    <a href="https://linkedin.com" class="!text-white hover:text-violet-500 transition"><i class="fa-brands fa-linkedin"></i></a>
    <a href="https://instagram.com" class="!text-white hover:text-violet-500 transition"><i class="fa-brands fa-instagram"></i></a>
  </div>
</section>

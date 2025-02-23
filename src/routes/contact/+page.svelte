<script>
    let name = "";
    let email = "";
    let message = "";
  
    function submitForm() {
      alert(`Thank you, ${name}! Your message has been received.`);
      // Here you can integrate an API to handle form submission.
    }
  </script>
  
  <section class="py-12 lg:py-20 flex flex-col items-center gap-10 text-center">
    <!-- Heading -->
    <div class="flex flex-col gap-2">
      <h6 class="text-lg sm:text-xl md:text-2xl">Get in Touch</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Let's <span class="poppins text-violet-400">Connect</span>
      </h3>
    </div>
  
    <!-- Contact Form -->
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
  
    <!-- Social Media Links -->
    <div class="flex gap-6 text-xl text-gray-300">
      <a href="https://facebook.com" class="hover:text-violet-500 transition"><i class="fa-brands fa-facebook"></i></a>
      <a href="https://twitter.com" class="hover:text-violet-500 transition"><i class="fa-brands fa-x-twitter"></i></a>
      <a href="https://linkedin.com" class="hover:text-violet-500 transition"><i class="fa-brands fa-linkedin"></i></a>
      <a href="https://instagram.com" class="hover:text-violet-500 transition"><i class="fa-brands fa-instagram"></i></a>
    </div>
  </section>
  
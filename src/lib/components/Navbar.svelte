<script>
  let isOpen = false;
</script>

<nav class="bg-gray-900 text-gray-50 shadow-lg">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between h-16 items-center">
     
      <div class="flex-shrink-0">
        <a href="/" class="text-xl font-bold tracking-wide hover:text-purple-400 !important">
          DevSphere
        </a>        
      </div>

      <div class="hidden md:flex space-x-6">
        <a href="/" class="relative !text-gray-50 transition duration-300 before:absolute before:-bottom-1 before:left-0 before:h-[2px] before:w-0 before:bg-purple-400 before:transition-all before:duration-300 hover:before:w-full">
          Home
        </a>
        
        <a href="/speakers" class="relative !text-gray-50 transition duration-300 before:absolute before:-bottom-1 before:left-0 before:h-[2px] before:w-0 before:bg-purple-400 before:transition-all before:duration-300 hover:before:w-full">
          Speakers
        </a>
        <a href="/schedule" class="relative !text-gray-50 transition duration-300 before:absolute before:-bottom-1 before:left-0 before:h-[2px] before:w-0 before:bg-purple-400 before:transition-all before:duration-300 hover:before:w-full">
          Schedule
        </a>
        <a href="/sponsors" class="relative !text-gray-50 transition duration-300 before:absolute before:-bottom-1 before:left-0 before:h-[2px] before:w-0 before:bg-purple-400 before:transition-all before:duration-300 hover:before:w-full">
          Sponsors
        </a>
        
        <a href="/contact" class="relative !text-gray-50 transition duration-300 before:absolute before:-bottom-1 before:left-0 before:h-[2px] before:w-0 before:bg-purple-400 before:transition-all before:duration-300 hover:before:w-full">
          Contact</a>

      <!-- Mobile Menu Button -->
      <button class="md:hidden focus:outline-none" on:click={() => isOpen = !isOpen}>
        {#if isOpen}
          <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        {:else}
          <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
          </svg>
        {/if}
      </button>
    </div>
  </div>

  <!-- Mobile Menu -->
  {#if isOpen}
    <div class="md:hidden bg-gray-800 py-2">
      <a href="/" class="block px-4 py-2 !text-gray-50 hover:text-purple-400">Home</a>
      <a href="/speakers" class="block px-4 py-2 !text-gray-50 hover:text-purple-400">Speakers</a>
      <a href="/schedule" class="block px-4 py-2 !text-gray-50 hover:text-purple-400">Schedule</a>
      <a href="/sponsors" class="block px-4 py-2 !text-gray-50 hover:text-purple-400">Sponsors</a>
      <a href="/contact" class="block px-4 py-2 !text-gray-50 hover:text-purple-400">Contact</a>
    </div>
  {/if}
</nav>
  
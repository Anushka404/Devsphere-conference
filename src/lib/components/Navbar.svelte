<script>
    import { onMount } from "svelte";
  
    let darkMode = false;
  
    // Check local storage for dark mode preference
    onMount(() => {
      darkMode = localStorage.getItem("theme") === "dark";
      updateTheme();
    });
  
    function toggleDarkMode() {
      darkMode = !darkMode;
      localStorage.setItem("theme", darkMode ? "dark" : "light");
      updateTheme();
    }
  
    function updateTheme() {
      if (darkMode) {
        document.documentElement.classList.add("dark");
      } else {
        document.documentElement.classList.remove("dark");
      }
    }
  </script>
  
  <nav class="bg-white dark:bg-gray-900 shadow-md fixed w-full z-10 top-0">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        
        <!-- Logo & Site Name -->
        <a href="/" class="flex items-center space-x-2 text-xl font-bold text-gray-900 dark:text-white">
          <img src="/logo.svg" alt="Logo" class="h-8 w-8" />
          <span>Devsphere Conference</span>
        </a>
  
        <!-- Navigation Links -->
        <div class="hidden md:flex space-x-6">
          <a href="/" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">Home</a>
          <a href="/speakers" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">Speakers</a>
          <a href="/schedule" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">Schedule</a>
          <a href="/sponsors" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">Sponsors</a>
          <a href="/about" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">About</a>
          <a href="/contact" class="text-gray-700 dark:text-gray-300 hover:text-blue-500">Contact</a>
        </div>
  
        <!-- Dark Mode Toggle -->
        <button
          class="ml-4 p-2 rounded-full bg-gray-200 dark:bg-gray-700 text-gray-800 dark:text-gray-100 hover:bg-gray-300 dark:hover:bg-gray-600"
          on:click={toggleDarkMode}
        >
          {darkMode ? "🌙" : "☀️"}
        </button>
  
        <!-- Mobile Menu Button -->
        <button class="md:hidden p-2 rounded-md focus:outline-none focus:ring-2 focus:ring-gray-400">
          ☰
        </button>
      </div>
    </div>
  </nav>
  
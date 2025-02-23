<script>
    import { speakers } from "$lib/data/speakers.js"; 
  </script>
  
  <section class="py-16 px-6 max-w-6xl mx-auto">
    <h2 class="text-5xl font-bold text-gray-900 dark:text-white text-center mb-12">Meet Our
    <span class="bg-gradient-to-t from-violet-200 to-violet-800 text-transparent bg-clip-text"> Speakers</span></h2>
  
    {#each speakers as speaker, i}
      <div class="flex flex-col md:flex-row items-center gap-8 mb-16 {i % 2 === 0 ? 'md:flex-row-reverse' : ''}">
        <img src={speaker.image} alt={speaker.name} 
          class="w-80 h-100 object-cover rounded-lg border-4 border-violet-700 shadow-lg" />

        <div class="text-center md:text-left max-w-lg">
          <h3 class="text-3xl font-semibold text-gray-900 dark:text-white">{speaker.name}</h3>
          <p class="text-lg text-violet-600 font-medium">{speaker.title}</p>
          <p class="mt-4 text-gray-600 dark:text-gray-400">{speaker.bio}</p>
        </div>
      </div>
    {/each}
  </section>
  
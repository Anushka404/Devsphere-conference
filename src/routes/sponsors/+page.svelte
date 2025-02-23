<script>
    let sponsors = {
      Gold: [
        { name: "Microsoft", logo: "/images/microsoft.png", link: "https://www.microsoft.com" },
        { name: "Google", logo: "/images/google.png", link: "https://www.google.com" }
      ],
      Silver: [
        { name: "Amazon", logo: "/images/amazon.png", link: "https://www.amazon.com" },
        { name: "IBM", logo: "/images/ibm.png", link: "https://www.ibm.com" }
      ],
      Bronze: [
        { name: "Intel", logo: "/images/intel.png", link: "https://www.intel.com" },
        { name: "NVIDIA", logo: "/images/nvidia.png", link: "https://www.nvidia.com" }
      ]
    };
  </script>
  
  <section class="py-12 text-center">
    <h2 class="text-5xl font-bold text-gray-900 dark:text-white">Our Sponsors</h2>
    
    {#each Object.keys(sponsors) as tier}
      <h3 class="text-3xl font-semibold mt-8 text-violet-700">{tier} Sponsors</h3>
      <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8 px-4 mt-4">
        {#each sponsors[tier] as sponsor}
          <a href={sponsor.link} target="_blank" class="block p-4 border rounded-lg shadow-lg hover:shadow-xl transition">
            <img class="w-40 h-40 mx-auto object-contain" src={sponsor.logo} alt={sponsor.name} />
            <p class="mt-2 text-lg font-medium text-gray-700 dark:text-white">{sponsor.name}</p>
          </a>
        {/each}
      </div>
    {/each}
  </section>
  
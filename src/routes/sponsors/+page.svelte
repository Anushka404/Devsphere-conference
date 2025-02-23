<script>
  import Sponsor from "$lib/components/Sponsor.svelte";

  let sponsors = {
    Gold: [
      { name: "Microsoft", icon: "fa-brands fa-windows", description: "Empowering the world with technology.", href: "https://www.microsoft.com" },
      { name: "Google", icon: "fa-brands fa-google", description: "Organizing the world's information.", href: "https://www.google.com" },
      { name: "Facebook", icon: "fa-brands fa-facebook", description: "Connecting people worldwide.", href: "https://www.facebook.com" },
    ],
    Silver: [
      { name: "Amazon", icon: "fa-brands fa-amazon", description: "Delivering everything, everywhere.", href: "https://www.amazon.com" },
      { name: "Apple", icon: "fa-brands fa-apple", description: "Innovating for a better future.", href: "https://www.apple.com" },
      { name: "Figma", icon: "fa-brands fa-figma", description: "Design, prototype, and collaborate.", href: "https://www.figma.com" }
    ],
    Bronze: [
      { name: "Pinterest", icon: "fa-brands fa-pinterest", description: "Inspiring creativity and ideas.", href: "https://www.pinterest.com" },
      
      { name: "Twitter", icon: "fa-brands fa-x-twitter", description: "What's happening in the world?", href: "https://www.twitter.com" },
      { name: "Spotify", icon: "fa-brands fa-spotify", description: "Music for every moment.", href: "https://www.spotify.com" }
    ]
  };
</script>

<section class="py-12 lg:py-20 flex flex-col gap-16">
  <div class="flex flex-col gap-2 text-center">
    <h6 class="text-lg sm:text-xl md:text-2xl">Our Sponsors</h6>
    <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
      Meet our <span class="poppins text-violet-400">partners</span>
    </h3>
  </div>

  {#each Object.entries(sponsors) as [tier, sponsors]}
    <div class="flex flex-col gap-6">
      <h4 class="text-2xl text-center p-8 font-bold text-white"> <span class="bg-gradient-to-b text-3xl from-violet-400 to-violet-700 text-transparent bg-clip-text">{tier}</span>  Sponsors:</h4>
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
        {#each sponsors as sponsor}
          <Sponsor sponsor={sponsor} />
        {/each}
      </div>
    </div>
  {/each}
</section>

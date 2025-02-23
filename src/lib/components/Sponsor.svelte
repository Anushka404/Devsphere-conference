<script>
    export let sponsor; // Using 'sponsor' instead of 'sponsers'
</script>

<a href={sponsor.href || "#"} target="_blank" 
   class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-violet-700 
          text-center group cursor-pointer hover:border-violet-400 duration-200 text-white">

    <!-- Icon Container -->
    <div class="bg-slate-950 place-items-center px-4 text-5xl md:text-6xl 
                -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200 text-white">
        <i class={sponsor.icon}></i>
    </div>

    <!-- Sponsor Name -->
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl text-white">{sponsor.name}</h3>

    <!-- Sponsor Description -->
    <p class="text-sm sm:text-base text-gray-300">{sponsor.description || "A trusted partner in technology."}</p>
    
    <slot />

    <!-- Go To Button -->
    <div class="flex flex-1 justify-between gap-4 items-center text-white">
        <div class="ml-auto cursor-pointer hover:text-slate-950 duration-200 hover:bg-violet-600
                    relative after:absolute after:top-0 after:right-full after:w-full
                    after:h-full after:bg-white after:duration-200 hover:after:translate-x-full 
                    after:z-[-1] overflow-hidden">
            <p class="relative z-4 text-white">Go to &rarr;</p>
        </div>
    </div>

</a>

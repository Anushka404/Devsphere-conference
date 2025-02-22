<script>
    export let title = "Devsphere Conference 2025";
    export let subtitle = "A must-attend event for developers and tech innovators.";
    export let date = "27/02/2025 - 28/02/2025";
    import CountdownTimer from "$lib/components/CountdownTimer.svelte";
    import SpeakerCard from "$lib/components/SpeakerCard.svelte";
    import { speakers } from "$lib/data/speakers.js";
</script>

    <main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
    <div
    class="mx-5 flex flex-col lg:flex-row items-center lg:items-start text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
    <div class="flex flex-col items-center lg:items-start">
        <span
            class="w-fit sm:w-auto bg-gradient-to-r from-indigo-500 to-violet-500 text-white px-4 py-1 rounded-full text-sm font-medium mx-auto lg:mx-0"
        >
            {date}
        </span>

        <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl leading-tight mt-4 lg:mt-6">
            Welcome to <span class="poppins tracking-tighter bg-gradient-to-b from-violet-200 to-violet-700 text-transparent bg-clip-text">Devsphere</span> Conference
            <br />
            <!-- Full Stack <span class="poppins text-violet-400">Developer</span> -->
        </h2>
        <p class="text-lg py-5 pb-5 text-gray-300">{subtitle}</p>

         <a class="blueShadow lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 mb-6">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
        <h4 class="relative z-9 text-black font-medium">Register Now &rarr;</h4>
        </a>

        
        </div>
        
    </div>
    <div class="relative shadow-2xl grid place-items-center">
        <img src="/images/hero2.avif" alt="Devsphere Conference" 
        class="hidden md:hidden lg:block object-cover z-[2] max-h-[70vh] rounded-3xl "
        />

    </div>
    
   
    </section>
    <div class="flex justify-center py-2 sm:py-10">
        <CountdownTimer /> 
    </div>
    
</main>
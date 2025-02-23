<script>
    // import { onMount } from 'svelte';
    import { speakers } from '$lib/data/speakers';
    import {schedule} from '$lib/data/schedule';
  import ScheduleCard from '$lib/components/ScheduleCard.svelte';


    let selectedDay = "Day 1";
    
    function filterSchedule(day) {
      selectedDay = day;
    }
  </script>
  
  <section class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col
  gap-16 sm:gap-20 md:gap-24 relative">
  <div class="flex flex-col gap-2 text-center relative
   before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5
    before:bg-violet-700
    after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5
    after:bg-violet-700 py-4
  ">
  <h6 class="text-lg sm:text-xl md:text-2xl">Want to stay updated?</h6>
  <h3 class="font-semibold text-3xl sm:text-4xl">
    Explore the <span class="poppins text-violet-400">schedule</span> and plan your sessions.</h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
        This is . . .
    </p>

    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
        {#each schedule as schedule, index}
        <div class="flex gap-6 sm:gap-8">
            <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
               <span class="text-2xl">Day</span> <br> 0{schedule.day}
               
            </p>
            
           
            <div class="flex flex-col gap-6 sm:gap-8">
                <h3 class="text-2xl sm:text-3xl md:text-5xl">
                    {schedule.topic}
                </h3>
                <p>
                    {schedule.description}
                </p>
            </div>
        </div>
        {/each}

    </div>
    <ScheduleCard/>
    
  </section>
  
  
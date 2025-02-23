<script>
    import { schedule } from "$lib/data/schedule.js";
  
    let activeDay = "All";
    let days = ["All", 1, 2, 3, 4, 5, 6]; 
  
    function filterSchedule(day) {
      activeDay = day;
    }
  </script>
  
  <section class="mt-10">
    
    <div class="flex justify-center space-x-4 mb-6">
      {#each days as day}
        <button 
          class="px-4 py-2 rounded-md transition-colors duration-200 text-sm sm:text-base
                 {activeDay === day ? 'bg-violet-700 text-white' : 'bg-gray-200 text-gray-800 hover:cursor-pointer hover:bg-violet-300 hover:text-black'}"
          on:click={() => filterSchedule(day)}
        >
          {day === "All" ? "All Days" : `Day ${day}`}
        </button>
      {/each}
    </div>
  
    <!-- Timetable -->
    <div class="overflow-x-auto">
      <table class="min-w-full bg-white border border-gray-300 shadow-md rounded-lg">
        <thead class="bg-violet-600 text-white">
          <tr>
            <th class="py-3 px-4 text-left">Date</th>
            <th class="py-3 px-4 text-left">Time</th>
            <th class="py-3 px-4 text-left">Topic</th>
            <th class="py-3 px-4 text-left">Speaker</th>
            <th class="py-3 px-4 text-left">Profile</th>
          </tr>
        </thead>
        <tbody>
          {#each schedule.filter(session => activeDay === "All" || session.day === activeDay) as session}
            <tr class="border-b border-gray-300 hover:bg-gray-100 text-gray-500">
              <td class="py-3 px-4">{session.date}</td>
              <td class="py-3 px-4">{session.time}</td>
              <td class="py-3 px-4 font-semibold">{session.topic}</td>
              <td class="py-3 px-4 text-gray-600">{session.speaker}</td>
              <td class="py-3 px-4">
                <img src={session.image} alt={session.speaker} class="w-12 h-12 rounded-full">
              </td>
            </tr>
          {/each}
        </tbody>
      </table>
    </div>
  </section>
  
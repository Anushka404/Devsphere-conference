<script>
    import { onMount } from "svelte";
    let days = 0, hours = 0, minutes = 0, seconds = 0;
    const eventDate = new Date("2025-02-27T00:00:00").getTime();
  
    function updateCountdown() {
      const now = new Date().getTime();
      const timeLeft = eventDate - now;
  
      if (timeLeft > 0) {
        days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
        hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
        seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
      }
    }
  
    onMount(() => {
      updateCountdown();
      const interval = setInterval(updateCountdown, 1000);
      return () => clearInterval(interval);
    });
  </script>
  
  <div class="  bg-gradient-to-b from-violet-950 to-black p-6 rounded-3xl shadow-lg text-center">
    <h3 class="text-lg font-semibold mb-2">The Countdown</h3>
    <div class="flex items-center justify-center gap-8">
    <div class="text-center">
      <span class="text-4xl font-bold">{days}</span>
      <p class="text-sm">Days</p>
    </div>
    <div class="text-center">
      <span class="text-4xl font-bold">{hours}</span>
      <p class="text-sm">Hours</p>
    </div>
    <div class="text-center">
      <span class="text-4xl font-bold">{minutes}</span>
      <p class="text-sm">Minutes</p>
    </div>
    <div class="text-center">
      <span class="text-4xl font-bold">{seconds}</span>
      <p class="text-sm">Seconds</p>
    </div>
    </div> 
  </div>
  
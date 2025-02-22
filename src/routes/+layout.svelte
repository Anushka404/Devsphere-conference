<script> 
  import Footer from "$lib/components/Footer.svelte"; 
  import Header from "$lib/components/Header.svelte";
  import "../app.css";

  let y = 0;
  let innerHeight = 0;
  let innerWidth = 0;

  function goTop() {
      document.body.scrollIntoView({ behavior: "smooth" });
  }
</script>

<div class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen">
  <!-- Scroll-to-top button -->
  <div class={"fixed bottom-10 right-10 duration-200 z-10 " + (y > 100 ? 'opacity-100 pointer-events-auto' : 'opacity-0 pointer-events-none')}>
      <button on:click={goTop} class="rounded-full bg-slate-900 text-violet-400 p-3 hover:bg-slate-800 cursor-pointer">
          <i class="fa-solid fa-arrow-up"></i>
      </button>
  </div>

  <Header {y} {innerHeight} />

  <!-- Slot for page content -->
  <main class="flex-1">
      <slot />
  </main>

  <Footer />
</div>

<!-- Bind scroll position -->
<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />



<script>
    import '@fontsource-variable/dm-sans';
    import Navbar from "../lib/components/Navbar.svelte";
    import Footer from "../lib/components/Footer.svelte";
    let { children } = $props();
    import "../app.css";
  </script>
  <Navbar />
  <!-- <Footer /> -->
  {@render children()}
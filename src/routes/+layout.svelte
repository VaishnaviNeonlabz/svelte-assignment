<script lang="ts">
  import '../app.css';
  import Footer from '$lib/components/Footer.svelte';
  import Navbar from '$lib/components/Navbar.svelte';
</script>

<div class="flex min-h-screen flex-col">
  <Navbar />
  <main class="flex-1">
    <slot />
  </main>
  <Footer />
</div>

<script>
  import Navbar from "$lib/components/Navbar.svelte";
</script>

<!-- Shared Navbar on all pages -->
<Navbar />

<!-- Render the specific page content here -->
<slot />

<!-- Optionally add a footer or other shared elements -->
<footer>
  <p>&copy; 2024 Titancore. All rights reserved.</p>
</footer>

<style>
  footer {
    text-align: center;
    padding: 1rem;
    background-color: #f0f0f0;
    position: absolute;
    width: 100%;
    bottom: 0;
  }
</style>

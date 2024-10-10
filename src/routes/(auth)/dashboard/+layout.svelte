
<script>
  import Sidebar from '$lib/components/Sidebar.svelte';
  import PortfolioBar from '$lib/components/PortfolioBar.svelte';
</script>

<div class="dashboard-layout">
  <Sidebar />
  <div class="dashboard-content">
    <slot /> 
  </div>
</div>

<style>
  .dashboard-layout {
    display: flex;
    height: 100vh; /* Ensures the layout takes up the full viewport height */
    overflow: hidden; /* Prevents scrolling on the entire layout */
  }

  .dashboard-content {
    flex-grow: 1;
    padding: 20px;
    background-color: #f4f4f4;
    overflow: hidden; /* Ensures no scrolling within the dashboard content */
  }
</style>

<script>
  // This is just a placeholder function. Replace with actual logout logic.
  const handleLogout = () => {
    // Perform logout operation here (e.g., clear tokens, call logout API)
    alert("You have been logged out");
    // Redirect the user after logout
    window.location.href = "/login"; // Or use SvelteKit's `goto('/login')`
  };
</script>

<nav class="sidebar">
  <ul>
    <li><a href="/dashboard">Dashboard</a></li>
    <li><a href="/dashboard/chart-box">Charts</a></li>
    <li><a href="/dashboard/place-order">Place Order</a></li>
    <li><a href="/dashboard/order-status">Order Status</a></li>
    <!-- Add more links as needed -->
  </ul>

  <!-- Logout Button -->
  <button class="logout-button" on:click={handleLogout}>Logout</button>
</nav>

<style>
  .sidebar {
    width: 150px;
    background-color: #ddd;
    padding: 20px;
    color: black;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100vh;
  }
  .sidebar ul {
    list-style-type: none;
    padding: 0;
  }

  .sidebar ul li {
    margin-bottom: 20px;
  }

  .sidebar ul li a {
    color: #000;
    text-decoration: none;
    font-size: 1.1rem;
  }

  .sidebar ul li a:hover {
    text-decoration: underline;
  }

  /* Logout button styling */
  .logout-button {
    margin-top: auto;
    margin-bottom: 50px;
    padding: 10px;
    background-color: #ff4d4d;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1rem;
  }

  .logout-button:hover {
    background-color: #e60000;
  }
</style>

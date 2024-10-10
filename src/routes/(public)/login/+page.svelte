<script>
  import { goto } from '$app/navigation'; // Import the goto function for redirection
  
  let username = '';
  let password = '';
  let errorMessage = '';
  
  // Handle form submission
  const handleSubmit = (event) => {
    event.preventDefault(); // Prevent form from refreshing the page

    if (!username || !password) {
      errorMessage = 'Please fill out both fields';
      return;
    }

    // Example of form submission logic
    // You would replace this with actual login logic (e.g., API call)
    if (username === 'admin' && password === 'password') {
      errorMessage = '';
      // Redirect to dashboard after successful login
      goto('/dashboard');
    } else {
      errorMessage = 'Invalid username or password';
    }
  };
</script>
  
  <style>

    h2 {
      margin-bottom: 20;
    }

    .login-container {
      max-width: 400px;
      margin: 0 auto;
      margin-top: 70px;
    }
  
    .input-field {
      display: block;
      width: 100%;
      padding: 12px;
      margin-bottom: 15px;
      border: none; /* Remove default border */
      border-bottom: 1px solid black; /* Only the bottom is underlined */
      outline: none; /* Remove outline on focus */
      font-size: 1rem;
    }
  
    .error-message {
      color: red;
      margin-bottom: 10px;
    }
  
    .login-button {
      display: block;
      width: 100%;
      padding: 10px;
      background-color: #000;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
  
    .login-button:hover {
      background-color: #333;
    }
  </style>
  
  <div class="login-container">
    <h2>Login</h2>
    {#if errorMessage}
      <div class="error-message">{errorMessage}</div>
    {/if}
    <form on:submit={handleSubmit}>
      <input
        class="input-field"
        type="text"
        placeholder="Username"
        bind:value={username}
      />
      <input
        class="input-field"
        type="password"
        placeholder="Password"
        bind:value={password}
      />
      <button class="login-button" type="submit">Login</button>
    </form>
  </div>
  
<!-- Navbar.svelte -->
<header class="navbar">
    <!-- Website Title -->
    <h1 class="website-title">Regressor</h1>
    
    <!-- Divider -->
    <hr class="divider" />
    
    <!-- Navigation Items -->
    <nav class="nav-items">
      <ul>
        <li><a href="/">Home</a></li>
        <!-- <li><a href="/founder">Founder</a></li> -->
        <li><a href="/login">Login</a></li>
        <li><a href="/contact">Contact</a></li>
        <!-- <li><a href="/disclaimers">Disclaimers</a></li> -->
      </ul>
    </nav>
  </header>
  
  <style>
    /* Styling for the navbar */
    .navbar {
      text-align: center;
      padding: 20px;
    }
  
    /* Website title */
    .website-title {
      font-size: 2.5rem;
      font-weight: bold;
      margin-bottom: 10px;
    }
  
    /* Divider (horizontal line) */
    .divider {
      border: 1px solid black;
      width: 80%;
      margin: 0 auto 20px auto;
    }
  
    /* Navigation items */
    .nav-items ul {
      list-style: none;
      padding: 0;
      display: flex;
      justify-content: center;
      gap: 50px;
    }
  
    .nav-items ul li {
      display: inline;
    }
  
    .nav-items ul li a {
      text-decoration: none;
      color: black;
      font-size: 1rem;
    }
  
    .nav-items ul li a:hover {
      text-decoration: underline;
    }
  </style>
  
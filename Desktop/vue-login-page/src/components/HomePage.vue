<template>
    <div>
      <!-- Header -->
      <header class="header">
        <div class="logo-container left">
          <img src="src/assets/agusandur1.png" alt="Logo 1" class="logo">
        </div>
        <div class="text-container">
          <h1>Barangay Name</h1>
          <h2>Municipality of Loreto <br> Province of Agusan del Sur</h2>
        </div>
        <div class="logo-container right">
          <img src="src/assets/loreto1.png" alt="Logo 2" class="logo">
        </div>
      </header>
  
      <!-- Navbar -->
      <nav class="navbar">
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </nav>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomePage',
  };
  </script>
  
  <style scoped>
  /* Container for the header */
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 20vh; /* 20% of the viewport height */
    padding: 0 20px;
    flex-wrap: wrap;
  }
  
  /* Left and right logo containers */
  .logo-container {
    flex: 0 0 auto;
  }
  
  .left {
    text-align: left;
  }
  
  .right {
    text-align: right;
  }
  
  /* Logos styling */
  .logo {
    max-width: 100%;
    height: auto;
    max-height: 80%; /* Ensures logos stay within the height limit */
  }
  
  /* Text container for the titles */
  .text-container {
    text-align: center;
    flex: 1;
  }
  
  h1 {
    margin: 0;
    font-size: 2em;
  }
  
  h2 {
    margin: 0;
    font-size: 1.2em;
  }
  
  /* Navbar styling */
  .navbar {
    background-color: #333;
    padding: 10px 0;
    text-align: center;
  }
  
  .navbar ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
  }
  
  .navbar ul li {
    display: inline;
    margin-right: 20px;
  }
  
  .navbar ul li a {
    color: white;
    text-decoration: none;
    font-size: 1.2em;
  }
  
  .navbar ul li a:hover {
    text-decoration: underline;
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    .header {
      flex-direction: column;
      height: auto;
      padding: 10px;
      justify-content: center;
      text-align: center;
    }
  
    .logo-container {
      margin-bottom: 10px;
    }
  
    .navbar ul li {
      display: block;
      margin: 10px 0;
    }
  
    .navbar ul li a {
      font-size: 1.5em;
    }
  }
  
  @media (max-width: 480px) {
    h1 {
      font-size: 1.6em;
    }
  
    h2 {
      font-size: 1em;
    }
  
    .navbar ul li a {
      font-size: 1.2em;
    }
  }
  </style>
  
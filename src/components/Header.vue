<template>
    <header class="header">
      <nav>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#features">Features</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: 'Header',
  };
  </script>
  
  <style scoped>
  .header {
    background-color: #333;
    color: white;
    padding: 1rem;
  }
  nav ul {
    list-style: none;
    display: flex;
    gap: 2rem;
  }
  nav ul li a {
    color: white;
    text-decoration: none;
  }
  </style>
  
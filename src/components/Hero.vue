<template>
    <section class="hero">
      <h1>Welcome to Our Landing Page</h1>
      <p>We offer amazing services to help you succeed.</p>
      <button>Get Started</button>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Hero',
  };
  </script>
  
  <style scoped>
  .hero {
    text-align: center;
    padding: 3rem;
    background-color: #f4f4f4;
  }
  button {
    padding: 1rem 2rem;
    background-color: #007bff;
    color: white;
    border: none;
    cursor: pointer;
  }
  button:hover {
    background-color: #0056b3;
  }
  </style>
  
<template>
    <section class="section-one">
      <div class="background-container"></div>
  
      <!-- Imagen Derecha -->
      <div class="right-image-container">
        <img src="../assets/section-one/Portada-ciclo-6.1.png" alt="Imagen derecha" class="responsive-image"/>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'SectionOne',
  }
  </script>
  
  <style scoped>
  .section-one {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden; /* Para evitar desbordamiento */
  }
  
  .background-container {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('../assets/section-one/Fondo-Portada-ciclo-6.png');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  
  .right-image-container {
    position: absolute;
    top: 0;
    right: 0;
    height: 100%; 
    width: 50%; 
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1; 
  }
  
  .responsive-image {
    width: 100%;
    height: 100%; 
    object-fit: cover; 
  }
  
  @media (min-width: 768px) and (max-width: 1024px), /* Tablets en modo retrato */
         (min-width: 1024px) and (max-width: 1366px) /* Tablets en modo paisaje */ {
    .section-one {
      height: 100vh;
    }
  
    .background-container {
      background-size: cover;
      background-position: center;
    }
  
    .right-image-container {
      width: 48%; 
    }
  }
  
  @media (max-width: 1024px) and (max-height: 768px) {
    .right-image-container {
      width: 55%;
    }
  }
  </style>
  
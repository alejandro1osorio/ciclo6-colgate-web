<template>
    <section class="section-one">
      <div class="background-container"></div>
  
      <!-- Imagen Derecha -->
      <div class="right-image-container">
        <img src="../assets/section-one/Portada-ciclo-6.1.png" alt="Imagen derecha" class="responsive-image" />
      </div>
  
      <!-- Imagen Inferior Izquierda -->
      <img src="../assets/section-one/Nube-Portada-ciclo-6.png" alt="Imagen inferior izquierda" class="bimg-responsive" />
  
      <!-- Texto en la esquina inferior izquierda -->
      <div class="text-container">
        <p class="responsive-text">
          En sus manos<br />
          está la posibilidad<br />
          de transformar sonrisas<br />
           y mejorar la calidad de vida<br />
          de muchas personas.
        </p>
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
    overflow: hidden; 
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
    width: 30%; 
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
  
  .bimg-responsive {
    position: absolute;
    bottom: 0; 
    left: 0; 
    width: 100%; 
    height: 95%; 
    object-fit: cover; 
    z-index: 1; 
  }
  
  .text-container {
    position: absolute;
    bottom: 50px; 
    left: 116px; 
    z-index: 2; 
    color: #B28236; 
  }
  
  .responsive-text {
    font-size: 2.9rem; 
    text-align: left; 
    margin: 0; 
  }
  
  /* Estilos responsivos */
  @media (max-width: 768px) {
    .responsive-text {
      font-size: 1.2rem; 
    }
  }
  
  @media (max-width: 480px) {
    .responsive-text {
      font-size: 1rem; 
    }
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
  
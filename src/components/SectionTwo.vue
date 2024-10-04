<template>
  <section class="responsive-section">
    <!-- Imagen en la esquina superior izquierda -->
    <img class="top-left-image" src="../assets/section-two/Logo Total.png" alt="Top Left Image" />

    <!-- Texto sobre la imagen central -->
    <h2 class="center-text">Ayuda a controlar la causa principal<br> de la mayoría de los problemas de<br> salud bucal.</h2>

    <!-- Contenedor para la imagen central -->
    <div class="image-container">
      <!-- Imagen central -->
      <img class="center-image" src="../assets/section-two/Diente_1.webp" alt="Center Image" />
    </div>

    <!-- Nueva imagen lateral fuera del contenedor de la imagen central -->
    <img class="side-image" src="../assets/section-two/Escudo.webp" alt="Side Image" />

    <!-- Imágenes a la izquierda -->
    <img class="left-image image-1" src="../assets/section-two/Caries_1.webp" alt="Left Image 1" />
    <img class="left-image image-2" src="../assets/section-two/Erosión de Esmalte.webp" alt="Left Image 2" />
    <img class="left-image image-3" src="../assets/section-two/Pigmentaciones_1.webp" alt="Left Image 3" />
    <img class="left-image image-4" src="../assets/section-two/Gingivitis.webp" alt="Left Image 4" />

    <!-- Imágenes a la derecha -->
    <img class="right-image image-5" src="../assets/section-two/Cálculos_2.webp" alt="Right Image 1" />
    <img class="right-image image-6" src="../assets/section-two/Placa_1.webp" alt="Right Image 2" />
    <img class="right-image image-7" src="../assets/section-two/Halitosis_1.webp" alt="Right Image 3" />
    <img class="right-image image-8" src="../assets/section-two/Sensibilidad_1.webp" alt="Right Image 4" />

    <!-- Textos debajo de la imagen central -->
    <div class="bottom-texts">
      <p class="light-font">Con protección antibacteriana por 24 horas***<br> clínicamente probada.</p>
      <p class="light-font">Ayuda a prevenir los problemas<br> antes de que aparezcan.</p>
      <p class="small-font">*Reducción de placa antes de que ocurran los problemas; ayuda a proteger el esmalte contra la erosión dental.<br> **Reducción de placa bacteriana, con 3 meses de uso continuo.<br> ***Con cepillado 2x día después de 4 semanas de uso contínuo.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectionResponsive",
};
</script>

<style scoped>
@font-face {
  font-family: 'ColgateReady-Light';
  src: url('../assets/fonts/ColgateReady-Light.ttf') format('truetype');
}

/* Estilos generales */
.responsive-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
  padding: 20px;
  width: 100%;
  min-height: 100vh;
  box-sizing: border-box;
}

/* Imagen en la esquina superior izquierda */
.top-left-image {
  position: absolute;
  top: 1px;
  left: 8px;
  width: 150px;
  height: auto;
}

/* Texto central encima de la imagen */
.center-text {
  font-family: 'ColgateReady-Light', sans-serif;
  text-align: center;
  font-size: 2rem;
  margin-bottom: 10px;
  font-weight: 100;
  color: #875315;
  line-height: 1;
}

/* Contenedor para la imagen central */
.image-container {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  width: fit-content;
  margin-bottom: 20px;
}

/* Imagen central */
.center-image {
  max-width: 400px; /* Mantener el tamaño original */
  height: auto;
}

/* Imagen lateral, fuera del contenedor */
.side-image {
  position: absolute;
  top: 50%;
  left: 70%; /* Ajustado más a la derecha */
  transform: translate(-50%, -30px); /* Mueve la imagen lateral un poco abajo */
  max-width: 150px;
  width: 30%; /* Ajusta el tamaño según sea necesario */
  height: auto;
}

/* Estilos para las imágenes a la izquierda */
.left-image {
  position: absolute;
  width: 180px; /* Tamaño deseado */
  height: auto; /* Mantiene la relación de aspecto */
}

/* Posicionamiento individual para cada imagen a la izquierda */
.image-1 {
  left: 29%;
  top: 27%;
}

.image-2 {
  width: 269px;
  left: 19%;
  top: 34%;
}

.image-3 {
  width: 291px;
  left: 17%;
  top: 40%;
}

.image-4 {
  left: 20%;
  top: 47%;
}

/* Estilos para las imágenes a la derecha */
.right-image {
  position: absolute;
  width: 180px; /* Tamaño deseado */
  height: auto; /* Mantiene la relación de aspecto */
}

/* Posicionamiento individual para cada imagen a la derecha */
.image-5 {
  width: 271px;
  right: 28%;
  top: 28%;
}

.image-6 {
  width: 287px;
  right: 22%;
  top: 35%;
}

.image-7 {
  width: 268px;
  right: 19%;
  top: 39%;
}

.image-8 {
  width: 358px;
  right: 17%;
  top: 59%;
}

/* Textos debajo de la imagen central */
.bottom-texts {
  text-align: center;
  max-width: 90%;
  margin: 0 auto;
}

.bottom-texts p {
  margin: 10px 0;
  word-wrap: break-word;
}

/* Aplica la tipografía ColgateReady-Light y el tamaño a los 2 primeros párrafos */
.bottom-texts p.light-font {
  font-family: 'ColgateReady-Light', sans-serif;
  color: #875315;
  font-size: 2.2rem;
  line-height: 1;
  padding-top: 10px;
}

/* Estilo para el último párrafo, el más pequeño */
.bottom-texts p.small-font {
  font-family: 'ColgateReady-Light', sans-serif;
  color: #4d4c4b;
  font-size: 0.8rem;
  line-height: 1;
  padding-top: 10px;
}

.center-text {
  margin-top: 90px; /* Márgen superior */
  margin-bottom: 50px; /* Márgen inferior */
}

/* Estilos responsive para tablets */
@media (min-width: 768px) and (max-width: 1024px) {
  .center-text {
    font-size: 2.2rem;
  }

  .center-image {
    max-width: 400px;
  }

  .side-image {
    left: 75%; /* Ajuste para tablets */
    max-width: 130px;
  }

  .bottom-texts p {
    font-size: 1.2rem;
  }

  .top-left-image {
    width: 150px;
  }
}

/* Estilos responsive generales para pantallas más grandes */
@media (min-width: 1025px) {
  .center-text {
    font-size: 2.5rem;
  }

  .center-image {
    max-width: 400px;
  }

  .side-image {
    left: 70%; /* Ajuste de la imagen lateral */
    max-width: 150px;
  }

  .bottom-texts p {
    font-size: 1.4rem;
  }

  .top-left-image {
    width: 290px;
  }
}
</style>

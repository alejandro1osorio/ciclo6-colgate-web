<template>
  <section class="responsive-section">
    <!-- Imagen en la esquina superior izquierda -->
    <img class="top-left-image" src="../assets/section-two/Logo Total.png" alt="Top Left Image" />

    <!-- Texto sobre la imagen central -->
    <h2 class="center-text">Ayuda a controlar la causa principal<br> de la mayoría de los problemas de<br> salud bucal.</h2>

    <!-- Imagen central -->
    <img class="center-image" src="../assets/section-two/Diente_1.webp" alt="Center Image" />

    <!-- Textos debajo de la imagen central -->
    <div class="bottom-texts">
      <p class="light-font">Con protección antibacteriana por 24 horas***<br> clínicamente probada.</p>
      <p class="light-font">Ayuda a prevenir los problemas<br> antes de que aparezcan.</p>
      <p>*Reducción de placa antes de que ocurran los problemas; ayuda a proteger el esmalte contra la erosión dental.<br> **Reducción de placa bacteriana, con 3 meses de uso continuo.<br> ***Con cepillado 2x día después de 4 semanas de uso contínuo.</p>
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
  left: 20px;
  width: 120px;
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

/* Imagen central */
.center-image {
  width: 60%;
  height: auto;
  max-width: 400px;
  margin-bottom: 20px;
}

/* Textos debajo de la imagen central */
.bottom-texts {
  text-align: center;
  max-width: 90%;
  margin: 0 auto;
}

.bottom-texts p {
  margin: 10px 0;
  font-size: 1rem;
  word-wrap: break-word;
}

/* Aplica la tipografía ColgateReady-Light solo a los dos primeros párrafos */
.light-font {
  font-family: 'ColgateReady-Light', sans-serif;
}

/* Estilos responsive para tablets */
@media (min-width: 768px) and (max-width: 1024px) {
  .center-text {
    font-size: 2.2rem;
  }

  .center-image {
    width: 50%;
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
    width: 40%;
  }

  .bottom-texts p {
    font-size: 1.4rem;
  }

  .top-left-image {
    width: 180px;
  }
}
</style>

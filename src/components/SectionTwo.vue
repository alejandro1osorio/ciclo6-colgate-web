<template>
  <section class="responsive-section">
    <!-- Imagen en la esquina superior izquierda -->
    <img class="top-left-image" src="../assets/section-two/Logo Total.png" alt="Top Left Image" />

    <!-- Texto sobre la imagen central -->
    <h2 class="center-text">Este es el texto sobre la imagen central</h2>

    <!-- Imagen central -->
    <img class="center-image" src="../assets/section-two/Diente_1.webp" alt="Center Image" />

    <!-- Textos debajo de la imagen central -->
    <div class="bottom-texts">
      <p>Texto 1</p>
      <p>Texto 2</p>
      <p>Texto 3</p>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectionResponsive",
};
</script>

<style scoped>
/* Estilos generales */
.responsive-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
  padding: 20px;
  width: 100%;
  height: 100vh;
  box-sizing: border-box;
}

/* Imagen en la esquina superior izquierda */
.top-left-image {
  position: absolute;
  top: 10px;
  left: 20px; /* Margen izquierdo ajustado */
  width: 80px; /* Ajustable según necesidades */
  height: auto;
}

/* Texto central encima de la imagen */
.center-text {
  text-align: center;
  font-size: 1.5rem;
  margin-bottom: 10px;
}

/* Imagen central */
.center-image {
  width: 60%; /* Ajuste del tamaño en porcentaje */
  height: auto;
  max-width: 400px; /* Tamaño máximo para tabletas */
  margin-bottom: 20px;
}

/* Textos debajo de la imagen central */
.bottom-texts {
  text-align: center;
}

.bottom-texts p {
  margin: 10px 0;
  font-size: 1rem;
}

/* Estilos responsive para tablets */
@media (min-width: 768px) and (max-width: 1024px) {
  .center-text {
    font-size: 1.8rem;
  }

  .center-image {
    width: 50%;
  }

  .bottom-texts p {
    font-size: 1.2rem;
  }
}

/* Estilos responsive generales para pantallas más grandes */
@media (min-width: 1025px) {
  .center-text {
    font-size: 2rem;
  }

  .center-image {
    width: 40%;
  }

  .bottom-texts p {
    font-size: 1.4rem;
  }
}
</style>

<template>
  <div class="responsive-section">
    <div class="background-image"></div>
    <div class="image-stack">
      <img src="../assets/section-nine/Cepillo.webp" class="img1" alt="Imagen 1" />
      <img src="../assets/section-nine/Crema dental.webp" class="img2" alt="Imagen 2" />
      <img src="../assets/section-nine/ENjuague.webp" class="img3" alt="Imagen 3" />
      <img src="../assets/section-nine/Sello_1.webp" class="img4" alt="Imagen 4" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionNine"
};
</script>

<style scoped>
.responsive-section {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url("../assets/section-nine/Fondo.webp");
  object-fit: cover;
  z-index: 1;
}

.image-stack {
  position: relative;
  width: 100%;
  height: 100%;
}

.img1 {
  position: absolute;
  z-index: 4;
  top: 20%;  /* Ubicación individual */
  right: 10%; /* Ubicación individual */
  width: 300px; /* Tamaño individual */
}

.img2 {
  position: absolute;
  z-index: 6;
  top: 10%;  /* Ubicación individual */
  right: 5%;  /* Ubicación individual */
  width: 320px; /* Tamaño individual */
}

.img3 {
  position: absolute;
  z-index: 3;
  top: 60%;  /* Ubicación individual */
  right: 20%; /* Ubicación individual */
  width: 280px; /* Tamaño individual */
}

.img4 {
  position: absolute;
  z-index: 5;
  top: 40%;  /* Ubicación individual */
  right: 15%; /* Ubicación individual */
  width: 310px; /* Tamaño individual */
}

/* Media queries para tablets, priorizando 1180x820 */
@media (max-width: 1180px) and (max-height: 820px) {
  .img1 {
    width: 150px; /* Tamaño reducido para imagen 1 */
    top: 15%; /* Ajuste individual */
    right: 8%; /* Ajuste individual */
  }
  
  .img2 {
    width: 160px; /* Tamaño reducido para imagen 2 */
    top: 12%; /* Ajuste individual */
    right: 5%; /* Ajuste individual */
  }

  .img3 {
    width: 140px; /* Tamaño reducido para imagen 3 */
    top: 55%; /* Ajuste individual */
    right: 18%; /* Ajuste individual */
  }

  .img4 {
    width: 170px; /* Tamaño reducido para imagen 4 */
    top: 35%; /* Ajuste individual */
    right: 12%; /* Ajuste individual */
  }
}

/* Otras resoluciones de tablet */
@media (min-width: 768px) and (max-width: 1024px) and (orientation: portrait),
       (min-width: 1024px) and (max-width: 1366px) and (orientation: landscape),
       (min-width: 800px) and (max-width: 1280px) and (orientation: portrait) {
  .img1 {
    width: 157px;
    top: 6%;
    right: 26%;
  }

  .img2 {
    width: 485px;
    top: 68%;
    right: 11%;
  }

  .img3 {
    width: 427px;
    top: 2%;
    right: -4%;
  }

  .img4 {
    width: 124px;
    top: 80%;
    right: 1%;
  }
}
</style>

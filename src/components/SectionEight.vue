<template>
  <div class="section-image">
    <!-- Imagen de fondo principal con rotación aplicada -->
    <img src="../assets/section-eight/líneas.webp" alt="Background" class="background" />

    <!-- Imagen 1 (flecha verde izquierda) -->
    <img src="../assets/section-eight/cepillo .webp" alt="Imagen 1" class="img-left" />

    <!-- Imagen 2 (flecha verde centro) -->
    <img src="../assets/section-eight/crema.webp" alt="Imagen 2" class="img-center" />

    <!-- Imagen 3 (flecha verde derecha) -->
    <img src="../assets/section-eight/Enjuague.webp" alt="Imagen 3" class="img-right" />

    <!-- Imagen de fondo duplicada con rotación aplicada -->
    <img src="../assets/section-eight/líneas.webp" alt="Background Overlay" class="background-overlay" />
  </div>
</template>

<script>
export default {
  name: 'SectionImage',
};
</script>

<style scoped>
.section-image {
  position: relative;
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.background {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  top: 54px;
  left: 0;
  z-index: 1;
  transform: rotate(378deg); /* Gira la imagen de fondo 15 grados */
}

.img-left {
  position: absolute;
  top: 38%;
  left: 31%;
  width: 9%;
  z-index: 2;
}

.img-center {
  position: absolute;
  top: 45%;
  left: 39%;
  width: 13%;
  z-index: 2;
}

.img-right {
  position: absolute;
  top: 26%;
  right: 26%;
  width: 23%;
  z-index: 3;
}

.background-overlay {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  top: 54px;
  left: 0;
  z-index: 3;
  transform: rotate(378deg); /* Gira la imagen de fondo duplicada 15 grados */
}
</style>

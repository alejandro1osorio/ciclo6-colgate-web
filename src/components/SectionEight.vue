<template>
  <div class="section-image">
    <!-- Imagen de fondo principal -->
    <img src="../assets/section-eight/líneas.webp" alt="Background" class="background" />

    <!-- Imagen 1 (flecha verde izquierda) -->
    <img src="../assets/section-eight/cepillo .webp" alt="Imagen 1" class="img-left" />

    <!-- Imagen 2 (flecha verde centro) -->
    <img src="../assets/section-eight/crema.webp" alt="Imagen 2" class="img-center" />

    <!-- Imagen 3 (flecha verde derecha) -->
    <img src="../assets/section-eight/Enjuague.webp" alt="Imagen 3" class="img-right" />

    <!-- Imagen de fondo duplicada con z-index más alto -->
    <img src="../assets/section-eight/líneas.webp" alt="Background" class="background-overlay" />
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
  top: 0;
  left: 0;
  z-index: 1;
}

.img-left {
  position: absolute;
  top: 20%;
  left: 15%;
  width: 10%;
  z-index: 2;
}

.img-center {
  position: absolute;
  top: 30%;
  left: 45%;
  width: 15%;
  z-index: 2;
}

.img-right {
  position: absolute;
  top: 25%;
  right: 10%;
  width: 12%;
  z-index: 2;
}

.background-overlay {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 3; /* Superior a las demás imágenes */
}
</style>

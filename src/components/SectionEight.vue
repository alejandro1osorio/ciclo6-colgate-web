<template>
  <div class="section-image">
    <!-- Imagen de fondo principal con rotación aplicada -->
    <img src="../assets/section-eight/lineas-regimen-total.png" alt="Background" class="background" />

    <!-- Imagen 1 (flecha verde izquierda) -->
    <img src="../assets/section-eight/cepillo .webp" alt="Imagen 1" class="img-left" />

    <!-- Imagen 2 (flecha verde centro) -->
    <img src="../assets/section-eight/crema.webp" alt="Imagen 2" class="img-center" />

    <!-- Imagen 3 (flecha verde derecha) -->
    <img src="../assets/section-eight/Enjuague.webp" alt="Imagen 3" class="img-right" />

    <!-- Imagen de fondo duplicada con rotación aplicada -->
    <img src="../assets/section-eight/lineas-regimen-total.png" alt="Background Overlay" class="background-overlay" />

    <!-- Nueva imagen centrada en la parte superior -->
    <img src="../assets/section-eight/Textos.webp" alt="Nueva Imagen" class="img-top-center" />

    <!-- Nueva imagen en la esquina inferior izquierda -->
    <img src="../assets/section-eight/Disclamer.webp" alt="Imagen Esquina Inferior Izquierda" class="img-bottom-left" />
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
    height: 110vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.background {
  width: 70%;
  height: 70%;
  position: absolute;
  top: 217px;
  left: 146px;
  z-index: 3;
  transform: rotate(365deg);
}

.img-left {
  position: absolute;
  top: 363px;
  left: 380px;
  width: 92px;
  z-index: 4;
}

.img-center {
  position: absolute;
  top: 374px;
  left: 449px;
  width: 13%;
  z-index: 3;
}

.img-right {
  position: absolute;
  top: 341px;
  right: 391px;
  width: 215px;
  z-index: 1;
}

.background-overlay {
  width: 70%;
  height: 70%;
  position: absolute;
  top: 217px;
  left: 146px;
  z-index: 4;
  transform: rotate(365deg); /* Gira la imagen de fondo duplicada */
}

.img-top-center {
  position: absolute;
  top: 16px;
  left: 50%;
  transform: translateX(-50%);
  width: 40%;
  z-index: 4;
}

/* Nueva imagen en la esquina inferior izquierda */
.img-bottom-left {
  position: absolute;
  bottom: -2px;
  left: 243px;
  width: 381px;
  z-index: 5;
}
</style>

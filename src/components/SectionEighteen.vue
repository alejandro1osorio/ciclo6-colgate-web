<template>
  <div class="section-eighteen">
    <!-- Logo Colgate -->
    <div class="logo-colgate">
      <img :src="require('@/assets/section-eighteen/logo-colgate-sensitive.webp')" alt="Colgate Logo" />
    </div>

    <!-- Imagen de los cepillos -->
    <div class="two-brushes">
      <img :src="require('@/assets/section-eighteen/2cepillos-blister.webp')" alt="Cepillos Colgate" />
    </div>

    <!-- Cabeza del cepillo -->
    <div class="brush-head">
      <img :src="require('@/assets/section-eighteen/3cabeza-cepillo.webp')" alt="Cabeza del Cepillo" />
    </div>

    <!-- Texto suavidad -->
    <div class="text-three">
      <img :src="require('@/assets/section-eighteen/4texto_3.webp')" alt="Texto Suavidad" />
    </div>

    <!-- Texto cerdas -->
    <div class="text-two">
      <img :src="require('@/assets/section-eighteen/5texto_2.webp')" alt="Texto Cerdas" />
    </div>

    <!-- Slider vertical con flechas -->
    <div class="slider-vertical">
      <div class="arrow up" @click="scrollUp">▲</div> <!-- Flecha superior -->
      <div class="slider-content" ref="sliderContent">
        <img :src="require('@/assets/section-eighteen/Cuadro-1.webp')" alt="Cuadro 1" />
        <img :src="require('@/assets/section-eighteen/Cuadro-2.webp')" alt="Cuadro 2" />
        <img :src="require('@/assets/section-eighteen/Cuadro-3.webp')" alt="Cuadro 3" />
        <img :src="require('@/assets/section-eighteen/Cuadro-4.webp')" alt="Cuadro 4" />
        <img :src="require('@/assets/section-eighteen/Cuadro-5.webp')" alt="Cuadro 5" />
      </div>
      <div class="arrow down" @click="scrollDown">▼</div> <!-- Flecha inferior -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionEighteen',
  methods: {
    scrollUp() {
      const slider = this.$refs.sliderContent;
      slider.scrollBy({ top: -150, behavior: 'smooth' }); // Desplazar hacia arriba
    },
    scrollDown() {
      const slider = this.$refs.sliderContent;
      slider.scrollBy({ top: 150, behavior: 'smooth' }); // Desplazar hacia abajo
    },
  },
};
</script>

<style scoped>
.section-eighteen {
  width: 1180px;
  height: 820px;
  position: relative;
  overflow: hidden; /* Evitar que los elementos se salgan del contenedor */
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  /* Imagen de fondo */
  background-image: url('@/assets/section-eighteen/fondo-sensitive.webp');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.logo-colgate {
  position: absolute;
  top: 0px;
  left: 20px;
  z-index: 4; /* Capa superior */
}

.logo-colgate img {
  width: 350px;
  height: auto;
}

.two-brushes {
  position: absolute;
  top: 140px;
  left: 45px;
  z-index: 5; /* Capa superior */
}

.two-brushes img {
  width: 150px;
  height: auto;
}

.brush-head {
  position: absolute;
  top: 100px;
  left: 61%;
  transform: translateX(-100%);
  z-index: 1; /* Colocar la imagen del cepillo en el fondo */
  opacity: 1;
}

.brush-head img {
  width: 800px;
  height: auto;
}

.text-three {
  position: absolute;
  top: 85px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 3; /* Colocar el texto por encima del cepillo */
}

.text-three img {
  max-width: 400px;
  height: auto;
}

.text-two {
  position: absolute;
  top: 625px;
  left: 53%;
  transform: translateX(-50%);
  z-index: 3; /* Colocar el texto por encima del cepillo */
}

.text-two img {
  max-width: 400px;
  height: auto;
}

/* Slider vertical */
.slider-vertical {
  position: absolute;
  top: -30px;
  right: 40px;
  width: 250px;
  height: calc(100% - 40px); /* Ajuste para mantener el slider dentro del contenedor */
  z-index: 4;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;

  /* Aplicar desvanecimiento en los bordes */
  mask-image: linear-gradient(to bottom, transparent 0%, black 10%, black 80%, transparent 100%);
}

.slider-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px; /* Espacio entre imágenes */
  overflow-y: auto;
  scroll-behavior: smooth;
}

/* Ocultar barra de desplazamiento */
.slider-content {
  scrollbar-width: none; /* Firefox */
}

.slider-content::-webkit-scrollbar {
  display: none; /* Chrome, Safari, Opera */
}

.slider-content img {
  width: 100%;
  height: auto;
}

/* Flechas para el slider */
.arrow {
  font-size: 24px;
  cursor: pointer;
  color: white;
}

.arrow.up {
  margin-bottom: 10px;
}

.arrow.down {
  margin-top: 10px;
}
</style>
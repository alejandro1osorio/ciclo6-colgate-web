<template>
  <sectionseventeen class="section-seventeen">
    <!-- Logo Colgate -->
    <sectionseventeen class="logo-colgate">
      <img :src="require('@/assets/section-seventeen/logo-colgate-sensitive.webp')" alt="Colgate Logo" />
    </sectionseventeen>

    <!-- Imagen de cremas en la parte superior derecha con animación -->
    <sectionseventeen class="cremas-img">
      <img :src="require('@/assets/section-seventeen/cremas.webp')" alt="Cremas" />
    </sectionseventeen>

    <!-- Slider vertical con flechas -->
    <sectionseventeen class="slider-vertical">
      <div class="arrow up" @click="scrollUp">▲</div> <!-- Flecha superior -->
      <div class="slider-content" ref="sliderContent">
        <div class="slide-item titulo">
          <img :src="require('@/assets/section-seventeen/titulo-1.webp')" alt="Título 1" />
        </div>
        <div class="slide-item diente">
          <img :src="require('@/assets/section-seventeen/1diente.webp')" alt="Diente" />
        </div>
        <div class="slide-item texto-1">
          <img :src="require('@/assets/section-seventeen/texto-1.webp')" alt="Texto 1" />
        </div>
        <div class="slide-item texto-2">
          <img :src="require('@/assets/section-seventeen/texto-2.webp')" alt="Texto 2" />
        </div>
        <div class="slide-item disclaimer">
          <img :src="require('@/assets/section-seventeen/disclamer_1.webp')" alt="Disclaimer 1" />
        </div>
      </div>
      <div class="arrow down" @click="scrollDown">▼</div> <!-- Flecha inferior -->
    </sectionseventeen>
  </sectionseventeen>
</template>

<script>
export default {
  name: 'SectionSeventeen',
  methods: {
    scrollUp() {
      const slider = this.$refs.sliderContent;
      slider.scrollBy({ top: -150, behavior: 'smooth' });
    },
    scrollDown() {
      const slider = this.$refs.sliderContent;
      slider.scrollBy({ top: 150, behavior: 'smooth' });
    },
  },
};
</script>

<style scoped>
.section-seventeen {
  width: 1180px;
  height: 100vh;
  background-image: url('@/assets/section-seventeen/fondo-sensitive.webp');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden; /* Evitar que los elementos sobresalgan */
}

.logo-colgate {
  position: absolute;
  top: 0px;
  left: 20px;
  z-index: 3;
}

.logo-colgate img {
  width: 350px;
  height: auto;
}

/* Animación de la imagen de cremas */
.cremas-img {
  position: absolute;
  top: 20px;
  right: -50px; /* Ajustar la imagen para que no sobresalga */
  z-index: 1;
  animation: breathing 3s ease-in-out infinite; /* Añadimos la animación */
}

.cremas-img img {
  width: 800px; /* Reducimos el tamaño de la imagen */
  height: auto;
}

/* Definición de la animación "breathing" */
@keyframes breathing {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.02); /* Crece un 2% */
  }
  100% {
    transform: scale(1); /* Vuelve a su tamaño original */
  }
}

/* Slider vertical */
.slider-vertical {
  width: 60%; /* Reducimos el ancho del slider para evitar desbordes */
  height: 100%;
  background-color: transparent;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  overflow: hidden;
  mask-image: linear-gradient(to bottom, transparent 10%, black 20%, black 85%, transparent 95%);
  margin-left: -500px;
}

.slider-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow-y: auto;
  scroll-behavior: smooth;
}

/* Ocultar barra de desplazamiento */
.slider-content {
  scrollbar-width: none;
}

.slider-content::-webkit-scrollbar {
  display: none;
}

/* Estilos para cada imagen dentro del slider */
.slide-item img {
  width: 100%;
  height: auto;
}

/* Estilos para imágenes en el slider */
.titulo img {
  width: 350px;
  margin-top: 130px;
}

.diente img {
  width: 280px;
  margin-top: -30px;
}

.texto-1 img {
  width: 500px;
  margin-top: 30px;
  margin-left: 100px;
}

.texto-2 img {
  width: 500px;
  margin-top: 1px;
  margin-left: 100px;
}

.disclaimer img {
  width: 500px;
  margin-top: 0px;
  margin-left: 100px;
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

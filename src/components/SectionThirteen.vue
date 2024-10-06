
<template>
  <section class="section-thirteen">
    <!-- Contenedor principal con fondo -->
    <div class="contenedor-principal">
      <!-- Fondo del contenedor -->
      <div class="fondo"></div>

      <!-- Imagen del cepillo alineada a la derecha -->
      <img
        class="imagen-cepillo"
        src="@/assets/section-thirteen/cabeza_cepillo_periogard2.webp"
        alt="Cabeza Cepillo"
      />

      <!-- Imagen derecha en el centro alineada a la derecha -->
      <img
        class="img-derecha"
        src="@/assets/section-thirteen/img_derecha.webp"
        alt="Imagen Derecha"
      />

      <!-- Imagen izquierda en el centro alineada a la izquierda -->
      <img
        class="img-izquierda"
        src="@/assets/section-thirteen/img_izquierda.webp"
        alt="Imagen Izquierda"
      />

      <!-- Nuevo slider centrado verticalmente y ubicado en la parte inferior -->
      <div class="slider-container">
        <div class="slider" ref="slider">
          <!-- Añadir las imágenes al slider -->
          <img
            class="slider-imagen slider-imagen-centrada item"
            src="@/assets/section-thirteen/texto_1.webp"
            alt="Texto 1"
          />
          <img
            class="slider-imagen slide item"
            src="@/assets/section-thirteen/texto_2.webp"
            alt="Texto 2"
          />
          <img
            class="slider-imagen slide item"
            src="@/assets/section-thirteen/texto_3.webp"
            alt="Texto 3"
          />
          <img
            class="slider-imagen slide item"
            src="@/assets/section-thirteen/texto_4.webp"
            alt="Texto 4"
          />
          <img
            class="slider-imagen slide item"
            src="@/assets/section-thirteen/texto_5.webp"
            alt="Texto 5"
          />
          <img
            class="slider-imagen slide item slider-imagen-oculta"
            src="@/assets/section-thirteen/texto_6.webp"
            alt="Texto 6"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectionThirteen',
  data() {
    return {};
  },
  methods: {
    scrollSlider(direction) {
      const slider = this.$refs.slider;
      if (direction === 'left') {
        slider.scrollBy({ left: -300, behavior: 'smooth' });
      } else if (direction === 'right') {
        slider.scrollBy({ left: 300, behavior: 'smooth' });
      }
    },
  },
};
</script>

<style scoped>
.section-thirteen {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #ffffff;
  position: relative;
  overflow: hidden;
}

.contenedor-principal {
  width: 100%;
  max-width: 1180px;
  height: 820px;
  max-height: 100vh;
  position: relative;
  overflow: hidden;
  z-index: 1;
}

.fondo {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('@/assets/section-thirteen/fondo_cepillo_periogard2.webp');
  background-size: cover;
  background-position: center;
  z-index: 1;
  animation: breathing-rotation 6s ease-in-out infinite; /* Combina la animación de respiración y rotación */
  transform-origin: center; /* Punto de ancla en el centro */
}

@keyframes breathing-rotation {
  0% {
    transform: scale(1) rotate(-2deg);
  }
  50% {
    transform: scale(1.03) rotate(2deg); /* Ajusta el valor para un efecto más sutil o más intenso */
  }
  100% {
    transform: scale(1) rotate(-2deg);
  }
}

.imagen-cepillo {
  position: absolute;
  top: 40%;
  right: 0px;
  transform: translateY(-50%);
  z-index: 2;
  width: 750px;
  height: auto;
  animation: cepillo-floating-breathing-rotation 6s ease-in-out infinite; /* Añadir la animación combinada de movimiento vertical, respiración y rotación */
  transform-origin: right center; /* Punto de ancla alineado a la derecha */
}

@keyframes cepillo-floating-breathing-rotation {
  0%, 100% {
    transform: scale(1) translateY(-50%) translateY(10px) rotate(0deg);
  }
  25% {
    transform: scale(1.04) translateY(-50%) translateY(5px) rotate(-2deg); /* Expansión y movimiento hacia abajo, rotación neutral */
  }
  50% {
    transform: scale(1.04) translateY(-50%) translateY(10px) rotate(0deg); /* Mantener el efecto en su punto máximo */
  }
  75% {
    transform: scale(1.04) translateY(-50%) translateY(5px) rotate(2deg); /* Volver al punto medio */
  }
}


.img-derecha {
  position: absolute;
  top: 88%;
  right: 50px;
  transform: translateY(-50%);
  z-index: 3;
  width: 25px;
  height: auto;
}

.img-izquierda {
  position: absolute;
  top: 88%;
  left: 50px;
  transform: translateY(-50%);
  z-index: 3;
  width: 25px;
  height: auto;
}

.slider-container {
  position: absolute;
  bottom: 25px;
  left: 50%;
  transform: translateX(-50%);
  width: 70%;
  height: 150px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  z-index: 4;
  mask-image: linear-gradient(to right, transparent, rgba(0, 0, 0, 1) 20%, rgba(0, 0, 0, 1) 80%, transparent);
  -webkit-mask-image: linear-gradient(to right, transparent, rgba(0, 0, 0, 1) 20%, rgba(0, 0, 0, 1) 80%, transparent);
}

.slider {
  display: flex;
  align-items: center;
  width: 100%;
  height: 100%;
  overflow-x: scroll;
  overflow-y: hidden;
  scroll-behavior: smooth;
  z-index: 5;
  gap: 50px; /* Añadido para mantener las imágenes equidistantes */
}

.slider::-webkit-scrollbar {
  display: none;
}

.slider {
  scrollbar-width: none;
}

.slider-imagen {
  max-height: 100%;
  width: auto;
  object-fit: contain;
}

.slider-imagen-centrada {
  margin: 180px; /* Centrar la primera imagen */
}

.slider-imagen-oculta {
  opacity: 0; /* Ocultar la imagen texto_6.webp */
}

.slide {
  position: relative;
}

.item {
  width: 500px;
  height: auto;
}
</style>
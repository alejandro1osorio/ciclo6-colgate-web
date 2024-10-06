<template>
  <sectionfifteen class="section-fifteen">
    <!-- Contenedor principal con el fondo -->
    <div class="contenedor-principal">
      <!-- Imagen de fondo -->
      <div class="fondo"></div>

      <!-- Mostrar Slider vertical con máscara de degradado solo cuando se haga clic en cuadro_3 -->
      <div v-if="showSlider" class="slider-vertical">
        <!-- Item 1: Texto Cuadros -->
        <div
          class="slide-item"
          :style="{
            width: imgSizes.textosCuadrosWidth,
            height: imgSizes.textosCuadrosHeight,
            transform: imgPositions.textosCuadrosTransform,
          }"
        >
          <img
            :src="require('@/assets/section-fifteen/textos_cuadros.webp')"
            alt="Textos Cuadros"
          />
        </div>

        <!-- Item 2: Banner Inferior -->
        <div
          class="slide-item"
          :style="{
            width: imgSizes.bannerInferiorWidth,
            height: imgSizes.bannerInferiorHeight,
            transform: imgPositions.bannerInferiorTransform,
          }"
        >
          <img
            :src="require('@/assets/section-fifteen/banner_inferior.webp')"
            alt="Banner Inferior"
          />
        </div>

        <!-- Item 3: Disclaimer -->
        <div
          class="slide-item"
          :style="{
            width: imgSizes.disclaimerWidth,
            height: imgSizes.disclaimerHeight,
            transform: imgPositions.disclaimerTransform,
          }"
        >
          <img
            :src="require('@/assets/section-fifteen/disclamer_2.webp')"
            alt="Disclaimer"
          />
        </div>
      </div>

      <!-- Imagen superior izquierda (texto.webp) -->
      <div class="imagen-texto-superior" v-if="showTexto" @click="mostrarCuadro1">
        <img
          :src="require('@/assets/section-fifteen/texto.webp')"
          alt="Texto Superior"
        />
      </div>

      <!-- Cuadro 1 -->
      <div
        class="imagen-cuadro cuadro-1"
        v-if="showCuadro1"
        @click="showNextCuadro(1)"
      >
        <img
          :src="require('@/assets/section-fifteen/cuadro_1.webp')"
          alt="Cuadro 1"
        />
      </div>

      <!-- Cuadro 2 -->
      <div
        class="imagen-cuadro cuadro-2"
        v-if="showCuadro2"
        @click="showNextCuadro(2)"
      >
        <img
          :src="require('@/assets/section-fifteen/cuadro_2.webp')"
          alt="Cuadro 2"
        />
      </div>

      <!-- Cuadro 3 -->
      <div
        class="imagen-cuadro cuadro-3"
        v-if="showCuadro3"
        @click="showSlider = true"
      >
        <img
          :src="require('@/assets/section-fifteen/cuadro_3.webp')"
          alt="Cuadro 3"
        />
      </div>

      <!-- Cuadro transparente sobre el centro del contenedor que activa la animación del enjuague -->
      <div v-if="showCuadroTransparente" class="cuadro-transparente" @click="activarAnimacionEnjuague"></div>

      <!-- Enjuague bucal en el centro, se moverá a su posición final con animación -->
      <div class="imagen-enjuague" ref="enjuague" @click="showTexto = true">
        <img
          :src="require('@/assets/section-fifteen/enjuague_2.webp')"
          alt="Enjuague Bucal"
        />
      </div>
    </div>
  </sectionfifteen>
</template>

<script>
export default {
  name: 'SectionFifteen',
  data() {
    return {
      // Control de visibilidad de los cuadros, slider y texto
      showCuadro1: false, // Inicialmente oculto hasta que se haga clic en texto.webp
      showCuadro2: false,
      showCuadro3: false,
      showSlider: false, // Control para mostrar el slider al hacer clic en cuadro_3
      showTexto: false,  // Control para mostrar el texto al hacer clic en enjuague_2.webp
      showCuadroTransparente: true, // Control para mostrar/ocultar cuadro transparente

      // Tamaños individuales de cada imagen en el slider
      imgSizes: {
        textosCuadrosWidth: '750px', // Tamaño de la imagen textos_cuadros.webp
        textosCuadrosHeight: 'auto',
        bannerInferiorWidth: '960px', // Tamaño de la imagen banner_inferior.webp
        bannerInferiorHeight: 'auto',
        disclaimerWidth: '700px', // Tamaño de la imagen disclamer_2.webp
        disclaimerHeight: 'auto',
      },

      // Posiciones individuales de cada imagen en el slider
      imgPositions: {
        textosCuadrosTransform: 'translate(-40px, 20px)', // Posición de la imagen textos_cuadros.webp
        bannerInferiorTransform: 'translate(10px, 100px)', // Posición de la imagen banner_inferior.webp
        disclaimerTransform: 'translate(-50px, 50px)', // Posición de la imagen disclamer_2.webp
      },
    };
  },
  methods: {
    showNextCuadro(currentCuadro) {
      if (currentCuadro === 1) {
        this.showCuadro2 = true;
      } else if (currentCuadro === 2) {
        this.showCuadro3 = true;
      }
    },
    // Método para mostrar cuadro 1 cuando se haga clic en texto.webp
    mostrarCuadro1() {
      this.showCuadro1 = true; // Mostrar cuadro_1
    },
    activarAnimacionEnjuague() {
      this.showCuadroTransparente = false; // Ocultar cuadro transparente después del clic
      const enjuagueElement = this.$refs.enjuague;
      enjuagueElement.classList.add('animacion-enjuague');
    },
  },
};
</script>

<style scoped>
.section-fifteen {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100vh;
  position: relative;
}

/* Contenedor principal de 1180x820px con el fondo */
.contenedor-principal {
  width: 1180px;
  height: 820px;
  position: relative;
  overflow: hidden;
  z-index: 2; /* Contenedor en un nivel por encima del slider */
}

/* Imagen de fondo */
/* Imagen de fondo */
.fondo {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('@/assets/section-fifteen/fondo_orthogar2.webp');
  background-size: cover;
  background-position: center;
  z-index: 1; /* Fondo en el nivel más bajo */
  animation: breathing 5s ease-in-out infinite; /* Añadir la animación en loop */
}

/* Definición de la animación "breathing" */
@keyframes breathing {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05); /* Crece un 2% */
  }
  100% {
    transform: scale(1);
  }
}

/* Slider vertical con máscara de degradado */
.slider-vertical {
  position: absolute;
  top: 430px;
  bottom: 40px;
  width: 980px;
  height: 250px;
  background-color: none;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  z-index: 1; /* Slider en el mismo nivel del fondo */

  /* Máscara de degradado en top y bottom */
  mask-image: linear-gradient(
    to bottom,
    transparent,
    rgba(0, 0, 0, 1) 10%,
    rgba(0, 0, 0, 1) 90%,
    transparent
  );
}

.slider-vertical::-webkit-scrollbar {
  display: none; /* Ocultar barra de desplazamiento en Chrome, Safari y Opera */
}

.slider-vertical {
  scrollbar-width: none; /* Ocultar barra de desplazamiento en Firefox */
}

/* Estilo de los items dentro del slider */
.slide-item {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 10px 0;
}

.slide-item img {
  max-width: 100%;
  height: auto;
}

/* Imagen superior izquierda (texto.webp) */
.imagen-texto-superior {
  position: absolute;
  top: 70px;
  left: 70px;
  z-index: 3;
  cursor: pointer; /* Indicar que es clickeable */
}
.imagen-texto-superior img {
  width: 550px;
  height: auto;
}

/* Cuadro 1 */
.cuadro-1 {
  position: absolute;
  top: 200px;
  left: 70px;
  z-index: 3;
}

.cuadro-1 img {
  width: 230px;
  height: auto;
}

/* Cuadro 2 */
.cuadro-2 {
  position: absolute;
  top: 200px;
  left: 330px;
  z-index: 3;
}

.cuadro-2 img {
  width: 238px;
  height: auto;
}

/* Cuadro 3 */
.cuadro-3 {
  position: absolute;
  top: 200px;
  left: 610px;
  z-index: 3;
}

.cuadro-3 img {
  width: 238px;
  height: auto;
}

/* Cuadro transparente para activar animación del enjuague */
.cuadro-transparente {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 500px;
  height: 500px;
  z-index: 5; /* Colocado por encima del enjuague para que sea clickeable */
  transform: translate(-50%, -50%);
  cursor: pointer;
  background-color: transparent;
}

/* Enjuague bucal inicialmente en el centro, con animación al activarse */
.imagen-enjuague {
  position: absolute;
  top: 50%;
  left: 50%;
  z-index: 4; /* Enjuague en un nivel superior */
  transform: translate(-50%, -50%);
}

.imagen-enjuague img {
  width: 510px;
  height: auto;
}

/* Definición de la animación para bajar desde el centro */
@keyframes bajarDesdeCentro {
  100% {
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0;
  }
  100% {
    top: -50px;                    /* Posición vertical final */
    right: 0;                      /* Alinear al borde derecho del contenedor */
    transform: translateX(30%);    /* Desplazar más hacia la derecha */
    opacity: 1;
  }
}


.animacion-enjuague {
  animation: bajarDesdeCentro 0.5s ease-out forwards;
}
</style>

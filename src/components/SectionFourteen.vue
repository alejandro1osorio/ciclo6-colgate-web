<template>
  <section class="section-fourteen">
    <!-- Contenedor principal de 1180x820px de color amarillo -->
    <div class="contenedor-principal">
      <!-- Fondo con la imagen -->
      <div class="fondo"></div>

      <!-- Imagen superior izquierda: textos_1.webp -->
      <img
        class="imagen-texto-superior"
        :src="require('@/assets/section-fourteen/textos_1.webp')"
        alt="Textos 1"
      />

      <!-- Imagen central: Aerosoles.webp con animación de opacidad -->
      <img
        class="imagen-central"
        :class="{ 'opacidad-activa': aplicarOpacidad }"
        :src="require('@/assets/section-fourteen/Aerosoles.webp')"
        alt="Aerosoles"
      />

      <!-- Imagen de enjuague en la parte central derecha con animación combinada -->
      <img
        class="imagen-enjuague animacion-combinada"
        :src="require('@/assets/section-fourteen/enjuague_1.webp')"
        alt="Enjuague"
        @click="activarOpacidad"
      />

      <!-- Disclaimer ubicado debajo de la imagen central -->
      <img
        class="imagen-disclaimer"
        :src="require('@/assets/section-fourteen/disclamer_1.webp')"
        alt="Disclamer"
      />

      <!-- Nueva imagen Sello_1.webp con animación controlada -->
      <img
        class="imagen-sello"
        :class="{ 'animacion-activa': aplicarAnimacionSello }"
        :src="require('@/assets/section-fourteen/Sello_1.webp')"
        alt="Sello"
      />
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectionFourteen',
  data() {
    return {
      aplicarOpacidad: false, // Controla si la imagen central tiene la animación de opacidad
      aplicarAnimacionSello: false, // Controla si la imagen Sello_1.webp tiene la animación
    };
  },
  methods: {
    activarOpacidad() {
      this.aplicarOpacidad = true; // Activa la animación de opacidad al hacer clic en el enjuague
      this.aplicarAnimacionSello = true; // Activa la animación de la imagen sello
    },
  },
};
</script>

<style scoped>
.section-fourteen {
  width: 100%;
  height: 100vh;
  display: flex; /* Utilizar flex para centrar correctamente el contenido */
  justify-content: center;
  align-items: center;
  background-color:none; /* Color amarillo */
  position: relative; /* Asegura que los hijos se posicionen relativamente a la sección */
  overflow: hidden; /* Asegura que no haya desbordes */
}

.contenedor-principal {
  width: 1180px;
  height: 820px;
  position: relative;
  overflow: hidden; /* Dejar ocultas partes fuera del contenedor */
  background-color: none; /* Color amarillo con algo de opacidad para asegurarse de que se vea */
  z-index: 2; /* Asegura que el contenedor esté por encima de otros elementos */
}

.fondo {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('@/assets/section-fourteen/fondo_periogard_enjuague.webp');
  background-size: cover;
  background-position: center;
  z-index: 1; /* El fondo debería estar en el nivel más bajo */
  animation: breathing 5s ease-in-out infinite; /* Animación tipo respiración */
}

@keyframes breathing {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.06); /* Crece un 6% */
  }
  100% {
    transform: scale(1);
  }
}

.imagen-texto-superior {
  position: absolute;
  top: 100px;
  left: 140px;
  z-index: 3; /* Asegura que esté por encima del fondo */
  width: 700px; /* Modificar tamaño */
  height: auto;
}

.imagen-central {
  position: absolute;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 4; /* Asegura que la imagen central esté visible por encima de los demás elementos */
  width: 1179px; /* Modificar tamaño */
  height: auto;
  opacity: 0; /* Inicialmente oculta */
  transition: opacity 1s ease-in-out; /* Transición suave para la opacidad */
}

.imagen-central.opacidad-activa {
  opacity: 1; /* Se muestra al activarse la clase */
}

.imagen-enjuague {
  position: absolute;
  top: 20px;
  right: 35px;
  transform: translateY(-50%);
  z-index: 6; /* Asegura que la imagen del enjuague esté visible y siempre al frente */
  width: 400px; /* Modificar tamaño */
  height: auto;
}

/* Animación combinada de respiración y wiggle */
.animacion-combinada {
  animation: wiggle-breathing 8s ease-in-out infinite;
}

@keyframes wiggle-breathing {
  0%, 100% {
    transform: scale(1) rotate(0deg);
  }
  25% {
    transform: scale(1.07) rotate(2deg);
  }
  50% {
    transform: scale(1.05) rotate(-1deg);
  }
  75% {
    transform: scale(1.07) rotate(0.6deg);
  }
}

.imagen-disclaimer {
  position: absolute;
  bottom: 45px; /* Cambiado para que esté más visible desde el fondo */
  left: 50%;
  transform: translateX(-50%);
  z-index: 6; /* Asegura que la imagen del disclaimer esté visible */
  width: 900px; /* Modificar tamaño */
  height: auto;
}

/* Nueva imagen Sello_1.webp */
.imagen-sello {
  position: absolute;
  top: 72%;
  left: 1024px;
  transform: translateY(-50%); /* Centra verticalmente la imagen sobre la imagen central */
  z-index: 10; /* Asegura que esté por encima de todos los elementos */
  width: 126px; /* Ajusta el tamaño de la imagen */
  height: auto;
  opacity: 0; /* Inicialmente oculta */
  transition: opacity 1s ease-in-out, transform 1s ease-in-out; /* Transiciones suaves */
}

/* Clase que se activará al hacer clic en la imagen del enjuague */
.imagen-sello.animacion-activa {
  opacity: 1; /* La imagen aparece */
  transform: translateY(-50%) scale(1.1); /* Pequeño zoom al aparecer */
}
</style>

<template>
  <div class="section-image">
    <!-- Contenedor transparente encima del contenedor principal -->
    <div class="contenedor-transparente"></div>

    <!-- Contenedor amarillo principal -->
    <div class="contenedor-amarillo">
      <!-- Imagen de fondo con animación de respiración y rotación -->
      <div class="fondo-animado"></div>

      <!-- Imágenes del cepillo y el enjuague, fuera del slider -->
      <div class="imagenes-externas">
        <div class="imagen-cepillo-wrapper">
          <img :src="require('@/assets/section-sixteen/cepillo.webp')" alt="Cepillo" class="imagen-cepillo" />
        </div>
        <div class="imagen-enjuague-wrapper">
          <img :src="require('@/assets/section-sixteen/enjuague.webp')" alt="Enjuague" class="imagen-enjuague" />
        </div>
      </div>

      <!-- Slider vertical que contiene las demás imágenes -->
      <div class="slider-vertical">
        <!-- Primera imagen: Texto de productos especializados -->
        <div class="slide-item texto-productos">
          <img :src="require('@/assets/section-sixteen/texto_1.webp')" alt="Texto Productos" />
        </div>
        <!-- Segunda imagen: Logo Orthogard -->
        <div class="slide-item logo-orthogard">
          <img :src="require('@/assets/section-sixteen/logo-orthogard.webp')" alt="Logo Orthogard" />
        </div>
        <!-- Banner del Cepillo y Enjuague centrados en el slider -->
        <div class="slide-item banner-item cepillo-banner">
          <img :src="require('@/assets/section-sixteen/cepillo-banner.webp')" alt="Cepillo Banner" />
        </div>
        <div class="slide-item banner-item enjuague-banner">
          <img :src="require('@/assets/section-sixteen/enjuague-banner.webp')" alt="Enjuague Banner" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionSixteen',
};
</script>

<style scoped>
.section-image {
  position: relative;
  width: 1180px;
  height: 820px;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Contenedor transparente de 500px por 820px, fijo en la parte superior */
.contenedor-transparente {
  position: absolute;
  top: 80px;
  left: 50%;
  width: 500px;
  height: 620px;
  background-color: rgba(255, 255, 255, 0); 
  transform: translateX(-50%);
  z-index: 2; 
}

/* Contenedor principal amarillo de 1180x820 */
.contenedor-amarillo {
  width: 1180px;
  height: 820px;
  background-color: lightgreen;
  position: relative;
  overflow: hidden; /* Para evitar que las imágenes se salgan del contenedor */
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Fondo con animación de respiración y rotación */
.fondo-animado {
  position: absolute;
  top: -10;
  left: -10;
  width: 107%;
  height: 107%;
  background-image: url('@/assets/section-sixteen/fondo_orthogar1.webp'); /* Imagen de fondo */
  background-size: cover;
  background-position: center;
  z-index: 0; /* Colocar la imagen de fondo detrás de todo */
  animation: breathing-rotation 5s ease-in-out infinite; /* Animación de respiración + rotación */
}

/* Animación de respiración y rotación del fondo */
@keyframes breathing-rotation {
  0% {
    transform: scale(1) rotate(-3deg); /* Inicio en -3 grados */
  }
  50% {
    transform: scale(1.05) rotate(3deg); /* Rotación de 3 grados y ligera expansión */
  }
  100% {
    transform: scale(1) rotate(-3deg); /* Regresa a la posición original */
  }
}

/* Flexbox para organizar las imágenes del cepillo y enjuague */
.imagenes-externas {
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 1; /* Estas imágenes estarán encima de la imagen de fondo */
}

.imagen-cepillo-wrapper, .imagen-enjuague-wrapper {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 2;
}

/* Permitir cambiar la posición del cepillo con animación de rotación */
.imagen-cepillo {
  width: 500px;
  height: auto;
  transform: var(--transform-cepillo, translate(300px, 160px)); /* Controlar la posición del cepillo */
  animation: rotarCepillo 3s infinite alternate ease-in-out; /* Animación de rotación */
  transition: transform 0.3s ease; /* Transición suave */
}

/* Permitir cambiar la posición del enjuague con animación de rotación inversa */
.imagen-enjuague {
  width: 500px;
  height: auto;
  transform: var(--transform-enjuague, translate(-330px, 130px)); /* Controlar la posición del enjuague */
  animation: rotarEnjuague 3s infinite alternate ease-in-out; /* Animación de rotación */
  transition: transform 0.3s ease; /* Transición suave */
}

/* Slider vertical */
.slider-vertical {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  overflow-y: scroll;
  overflow-x: hidden; /* Evitar el desplazamiento horizontal */
  scroll-behavior: smooth;
  z-index: 1; /* El slider estará por encima del cepillo y el enjuague */
}

/* Estilos para cada imagen dentro del slider */
.slide-item {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 820px; /* Cada imagen ocupa el tamaño completo del contenedor */
  position: relative;
  /* Permitir mover las imágenes dentro del slider */
  transform: var(--transform, translate(0, 0)); /* Usamos una variable CSS para mover cada imagen */
}

.slide-item img {
  max-width: var(--img-width, 100%);
  max-height: var(--img-height, 100%);
}

/* Estilos para el texto de productos */
.texto-productos {
  --transform: translate(-250px, 70px); /* Mover horizontal y verticalmente */
  --img-width: 500px; /* Tamaño del texto */
}

/* Estilos para el logo Orthogard */
.logo-orthogard {
  --transform: translate(300px, -70px); /* Solo mover verticalmente si es necesario */
  --img-width: 240px; /* Tamaño del logo */
}

/* Estilos para cepillo-banner */
.cepillo-banner {
  --transform: translate(350px, 535px); /* Mover horizontal y verticalmente el cepillo-banner */
  --img-width: 360px; /* Tamaño del cepillo-banner */
  margin-bottom: 0px;
}

/* Estilos para enjuague-banner */
.enjuague-banner {
  --transform: translate(-350px, 69px); /* Mover horizontal y verticalmente el enjuague-banner */
  --img-width: 350px; /* Tamaño del enjuague-banner */
  margin-bottom: 220px;
}

/* Animación de rotación del cepillo */
@keyframes rotarCepillo {
  0% {
    transform: translate(300px, 160px) rotate(-3deg);
  }
  100% {
    transform: translate(300px, 160px) rotate(3deg);
  }
}

/* Animación de rotación inversa del enjuague */
@keyframes rotarEnjuague {
  0% {
    transform: translate(-330px, 130px) rotate(3deg);
  }
  100% {
    transform: translate(-330px, 130px) rotate(-3deg);
  }
}

/* Ocultar barra de desplazamiento */
.slider-vertical::-webkit-scrollbar {
  display: none;
}

.slider-vertical {
  scrollbar-width: none; /* Firefox */
}
</style>
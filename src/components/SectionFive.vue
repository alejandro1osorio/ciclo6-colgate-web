<template>
  <div class="section-container">
    <!-- Checkbox oculto para activar la secuencia -->
    <input type="checkbox" id="trigger" class="hidden-checkbox" />

    <!-- Imagen de fondo que actúa como disparador (label para el checkbox) -->
    <label for="trigger">
      <img src="../assets/section-five/Plegadiza crema.png" alt="background" class="background-img trigger-img" />
    </label>

    <!-- Imagen centrada en la parte superior -->
    <img src="../assets/section-five/titulo-de-beneficios.webp" alt="imagen superior" class="image-superior img-titulo" />
    <img src="../assets/section-five/Beneifcios.png" alt="imagen superior" class="image-superior img-beneficios hidden" />

    <!-- Imagen 1 a Imagen 8 (visibilidad controlada por CSS) -->
    <img src="../assets/section-five/1.webp" alt="imagen 1" class="image image-1 hidden" />
    <img src="../assets/section-five/2.webp" alt="imagen 2" class="image image-2 hidden" />
    <img src="../assets/section-five/3.webp" alt="imagen 3" class="image image-3 hidden" />
    <img src="../assets/section-five/4.webp" alt="imagen 4" class="image image-4 hidden" />
    <img src="../assets/section-five/5.webp" alt="imagen 5" class="image image-5 hidden" />
    <img src="../assets/section-five/6.webp" alt="imagen 6" class="image image-6 hidden" />
    <img src="../assets/section-five/7.webp" alt="imagen 7" class="image image-7 hidden" />
    <img src="../assets/section-five/8.webp" alt="imagen 8" class="image image-8 hidden" />

    <!-- Imágenes conectadas al desencadenador después de Placa.png -->
    <img src="../assets/section-five/Placa.png" alt="imagen 9" class="image image-9 hidden-trigger" />
    <img src="../assets/section-five/Condiciones de encías_1.webp" alt="imagen 10" class="image image-10 hidden-trigger" />
    <img src="../assets/section-five/Halitosis.png" alt="imagen 11" class="image image-11 hidden-trigger" />
    <img src="../assets/section-five/Cálculos_1.webp" alt="imagen 12" class="image image-12 hidden-trigger" />
    <img src="../assets/section-five/Erosión del esmalte.png" alt="imagen 13" class="image image-13 hidden-trigger" />
    <img src="../assets/section-five/Caries.png" alt="imagen 14" class="image image-14 hidden-trigger" />
    <img src="../assets/section-five/Pigmentaciones.png" alt="imagen 15" class="image image-15 hidden-trigger" />
    <img src="../assets/section-five/Sensibilidad.png" alt="imagen 16" class="image image-16 hidden-trigger" />

    <!-- Imagen Disclamer en la parte inferior centrada -->
    <img src="../assets/section-five/Disclamer.png" alt="imagen disclamer" class="image image-disclamer" />
  </div>
</template>

<script>
export default {
  name: 'SectionComponent',
};
</script>

<style scoped>
.section-container {
  background-color: #fff;
  position: relative;
  width: 100%;
  height: 109vh;
  overflow: hidden;
}

/* Checkbox oculto */
.hidden-checkbox {
  display: none;
}

/* Imagen de fondo centrada y posicionada hacia abajo con animación de respiración */
.background-img {
  position: absolute;
  top: 458px; /* Ajusta este valor para posicionarla un poco hacia abajo */
  width: auto;
  height: auto;
  z-index: 21; /* La imagen de fondo está por encima de todas las otras imágenes */
  left: 50%;
  transform: translateX(-50%);
  cursor: pointer; /* Indica que es interactiva */
  animation: breathing 3s ease-in-out infinite; /* Animación de respiración */
}

/* Animación de respiración */
@keyframes breathing {
  0%, 100% {
    transform: translateX(-50%) scale(1);
  }
  50% {
    transform: translateX(-50%) scale(1.05);
  }
}

/* Permitir modificar la posición y tamaño de la imagen titulo-de-beneficios.webp */
.img-titulo {
  top: 90px;
  left: 50%;
  width: 750px;
  height: auto;
  position: absolute;
  transform: translateX(-50%);
  z-index: 22;
}

/* Permitir modificar la posición y tamaño de la imagen Beneifcios.png */
.img-beneficios {
  top: 120px;
  left: 37%;
  width: 250px;
  height: auto;
  position: absolute;
}

/* Estilos específicos para ocultar y mostrar las imágenes al activar el checkbox */
.hidden-checkbox:checked ~ .img-titulo {
  display: none;
}

.hidden-checkbox:checked ~ .img-beneficios {
  opacity: 1;
  transition: opacity 1s ease-in-out;
}

/* Mostrar imágenes conectadas al desencadenador */
.hidden-checkbox:checked ~ .hidden-trigger {
  opacity: 1;
  transition: opacity 1s ease-in-out;
}

/* Mostrar imágenes secuenciales después de Placa.png */
.hidden-checkbox:checked ~ .image-9 {
  opacity: 1;
  transition: opacity 1s ease-in-out;
}

.hidden-checkbox:checked ~ .image-9 ~ .image-10 {
  opacity: 1;
  transition: opacity 1s ease-in-out;
  transition-delay: 1s;
}

.hidden-checkbox:checked ~ .image-10 ~ .image-11 {
  opacity: 1;
  transition: opacity 1s ease-in-out;
  transition-delay: 2s;
}

.hidden-checkbox:checked ~ .image-11 ~ .image-12 {
  opacity: 1;
  transition: opacity 1s ease-in-out;
  transition-delay: 3s;
}

.hidden-checkbox:checked ~ .image-12 ~ .image-13 {
  opacity: 1;
  transition: opacity 1s ease-in-out;
  transition-delay: 4s;
}

.hidden-checkbox:checked ~ .image-13 ~ .image-14 {
  opacity: 1;
  transition: opacity 1s ease-in-out;
  transition-delay: 5s;
}

.hidden-checkbox:checked ~ .image-14 ~ .image-15 {
  opacity: 1;
  transition: opacity 1s ease-in-out;
  transition-delay: 6s;
}

.hidden-checkbox:checked ~ .image-15 ~ .image-16 {
  opacity: 1;
  transition: opacity 1s ease-in-out;
  transition-delay: 7s;
}

/* Estilos generales para las imágenes ocultas */
.hidden {
  opacity: 0;
  transition: opacity 1s ease-in-out;
  pointer-events: none;
}

/* Mostrar imagen cuando el checkbox está seleccionado */
.hidden-checkbox:checked ~ .image-1 {
  opacity: 1;
}

.hidden-checkbox:checked ~ .image-1 ~ .image-2 {
  opacity: 1;
  transition-delay: 1s;
}

.hidden-checkbox:checked ~ .image-2 ~ .image-3 {
  opacity: 1;
  transition-delay: 2s;
}

.hidden-checkbox:checked ~ .image-3 ~ .image-4 {
  opacity: 1;
  transition-delay: 3s;
}

.hidden-checkbox:checked ~ .image-4 ~ .image-5 {
  opacity: 1;
  transition-delay: 4s;
}

.hidden-checkbox:checked ~ .image-5 ~ .image-6 {
  opacity: 1;
  transition-delay: 5s;
}

.hidden-checkbox:checked ~ .image-6 ~ .image-7 {
  opacity: 1;
  transition-delay: 6s;
}

.hidden-checkbox:checked ~ .image-7 ~ .image-8 {
  opacity: 1;
  transition-delay: 7s;
}

/* Estilos para posicionar las imágenes */
.image {
  position: absolute;
}

.image-1 {
  top: 544px;
  left: 227px;
  z-index: 2;
}

.image-2 {
  top: 408px;
  left: 234px;
  z-index: 3;
}

.image-3 {
  top: 316px;
  left: 300px;
  z-index: 4;
}

.image-4 {
  top: 284px;
  left: 423px;
  z-index: 5;
}

.image-5 {
  top: 284px;
  left: 580px;
  z-index: 6;
}

.image-6 {
  top: 317px;
  left: 582px;
  z-index: 7;
}

.image-7 {
  top: 410px;
  left: 581px;
  z-index: 8;
}

.image-8 {
  top: 546px;
  left: 581px;
  z-index: 9;
}

/* Estilos para las imágenes conectadas al desencadenador */
.image-9 {
  top: 575px;
  left: 38px;
  z-index: 10;
  width: 196px;
  opacity: 0; /* Inicialmente oculto */
  transition: opacity 1s ease-in-out;
}

.image-10 {
  top: 430px;
  left: 56px;
  z-index: 11;
  width: 196px;
  opacity: 0; /* Inicialmente oculto */
  transition: opacity 1s ease-in-out;
}

.image-11 {
  top: 319px;
  left: 167px;
  z-index: 12;
  width: 196px;
  opacity: 0; /* Inicialmente oculto */
  transition: opacity 1s ease-in-out;
}

.image-12 {
  top: 256px;
  left: 300px;
  z-index: 13;
  width: 196px;
  opacity: 0; /* Inicialmente oculto */
  transition: opacity 1s ease-in-out;
}

.image-13 {
  top: 252px;
  left: 624px;
  z-index: 14;
  width: 196px;
  opacity: 0; /* Inicialmente oculto */
  transition: opacity 1s ease-in-out;
}

.image-14 {
  top: 313px;
  left: 809px;
  z-index: 15;
  width: 196px;
  opacity: 0; /* Inicialmente oculto */
  transition: opacity 1s ease-in-out;
}

.image-15 {
  top: 384px;
  left: 882px;
  z-index: 16;
  width: 196px;
  opacity: 0; /* Inicialmente oculto */
  transition: opacity 1s ease-in-out;
}

.image-16 {
  top: 574px;
  left: 937px;
  z-index: 17;
  width: 196px;
  opacity: 0; /* Inicialmente oculto */
  transition: opacity 1s ease-in-out;
}

/* Estilos para la imagen Disclamer en la parte inferior centrada */
.image-disclamer {
  bottom: 40px;
  left: 50%;
  width: 300px;
  height: auto;
  position: absolute;
  transform: translateX(-50%);
  z-index: 23;
  opacity: 100;
  transition: opacity 1s ease-in-out;
}
</style>

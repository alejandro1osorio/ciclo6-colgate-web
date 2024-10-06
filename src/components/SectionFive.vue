<template>
  <div class="section-container">
    <!-- Imagen de fondo, ahora centrada horizontalmente y posicionada por encima de las otras imágenes -->
    <img src="../assets/section-five/Plegadiza crema.png" alt="background" class="background-img" />

    <!-- Imagen centrada en la parte superior -->
    <img src="../assets/section-five/titulo-de-beneficios.webp" alt="imagen superior" class="image-superior" />
    <img src="../assets/section-five/Beneifcios.png" alt="imagen superior" class="image-superior img-sup-2" />

    <!-- Imagen 1 -->
    <img src="../assets/section-five/1.webp" alt="imagen 1" class="image image-1" />
    
    <!-- Imagen 2 -->
    <img src="../assets/section-five/2.webp" alt="imagen 2" class="image image-2" />
    
    <!-- Imagen 3 -->
    <img src="../assets/section-five/3.webp" alt="imagen 3" class="image image-3" />
    
    <!-- Imagen 4 -->
    <img src="../assets/section-five/4.webp" alt="imagen 4" class="image image-4" />
    
    <!-- Imagen 5 -->
    <img src="../assets/section-five/5.webp" alt="imagen 5" class="image image-5" />
    
    <!-- Imagen 6 -->
    <img src="../assets/section-five/6.webp" alt="imagen 6" class="image image-6" />
    
    <!-- Imagen 7 -->
    <img src="../assets/section-five/7.webp" alt="imagen 7" class="image image-7" />
    
    <!-- Imagen 8 -->
    <img src="../assets/section-five/8.webp" alt="imagen 8" class="image image-8" />
    
    <!-- Imagen 9 -->
    <img src="../assets/section-five/Placa.png" alt="imagen 9" class="image image-9" />
    
    <!-- Imagen 10 -->
    <img src="../assets/section-five/Condiciones de encías_1.webp" alt="imagen 10" class="image image-10" />
    
    <!-- Imagen 11 -->
    <img src="../assets/section-five/Halitosis.png" alt="imagen 11" class="image image-11" />
    
    <!-- Imagen 12 -->
    <img src="../assets/section-five/Cálculos_1.webp" alt="imagen 12" class="image image-12" />
    
    <!-- Imagen 13 -->
    <img src="../assets/section-five/Erosión del esmalte.png" alt="imagen 13" class="image image-13" />
    
    <!-- Imagen 14 -->
    <img src="../assets/section-five/Caries.png" alt="imagen 14" class="image image-14" />
    
    <!-- Imagen 15 -->
    <img src="../assets/section-five/Pigmentaciones.png" alt="imagen 15" class="image image-15" />
    
    <!-- Imagen 16 -->
    <img src="../assets/section-five/Sensibilidad.png" alt="imagen 16" class="image image-16" />
    
    <!-- Imagen 17 -->
    <img src="../assets/section-five/Disclamer.png" alt="imagen 17" class="image image-17" />
    
    <!-- Imagen 18 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 18" class="image image-18" /> -->

    <!-- Imagen 19 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 19" class="image image-19" /> -->
  </div>
</template>

<script>
export default {
  name: 'SectionComponent',
};
</script>

<style scoped>
.section-container {
  background-color: #fff; /*#5e6766*/
  position: relative;
  width: 100%;
  height: 109vh;
  overflow: hidden;
}

/* Imagen de fondo centrada y posicionada hacia abajo */
.background-img {
  position: absolute;
  top: 458px; /* Ajusta este valor para posicionarla un poco hacia abajo */
  width: auto;
  height: auto;
  z-index: 21; /* La imagen de fondo está por encima de todas las otras imágenes */
  left: 50%;
  transform: translateX(-50%);
}

/* Imagen centrada en la parte superior */
.image-superior {
  position: absolute;
  top: 60px; /* Puedes ajustar este valor para cambiar la altura */
  left: 50%;
  transform: translateX(-50%);
  z-index: 22; /* Asegura que esté por encima de las demás imágenes */
  width: 534px;
  height: auto;
}

.img-sup-2 {
  width: 247px;
  top: 90px;
}

/* Estilos para las demás imágenes, cada una con un z-index diferente */
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

.image-9 {
  top: 575px;
  left: 38px;
  z-index: 10;
  width: 196px;
}

.image-10 {
  top: 430px;
  left: 56px;
  z-index: 11;
  width: 196px;
}

.image-11 {
  top: 319px;
  left: 167px;
  z-index: 12;
  width: 196px;
}

.image-12 {
  top: 256px;
  left: 300px;
  z-index: 13;
  width: 196px;
}

.image-13 {
  top: 252px;
  left: 624px;
  z-index: 14;
  width: 196px;
}

.image-14 {
  top: 313px;
  left: 809px;
  z-index: 15;
  width: 196px;
}

.image-15 {
  top: 384px;
  left: 882px;
  z-index: 16;
  width: 196px;
}

.image-16 {
  top: 574px;
  left: 937px;
  z-index: 17;
  width: 196px;
}

.image-17 {
  top: 760px;
  left: 427px;
  z-index: 18;
  width: 350px;
}

.image-18 {
  top: 560px;
  left: 900px;
  z-index: 19;
}

.image-19 {
  top: 590px;
  left: 1000px;
  z-index: 20;
}
</style>

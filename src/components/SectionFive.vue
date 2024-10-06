<template>
  <div class="section-container">
    <!-- Imagen de fondo, ahora centrada horizontalmente y posicionada por encima de las otras imágenes -->
    <img src="../assets/section-five/Plegadiza crema.png" alt="background" class="background-img" />

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
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 9" class="image image-9" /> -->
    
    <!-- Imagen 10 -->
   <!--  <img src="../assets/section-five/1.webp" alt="imagen 10" class="image image-10" /> -->
    
    <!-- Imagen 11 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 11" class="image image-11" /> -->
    
    <!-- Imagen 12 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 12" class="image image-12" /> -->
    
    <!-- Imagen 13 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 13" class="image image-13" /> -->
    
    <!-- Imagen 14 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 14" class="image image-14" /> -->
    
    <!-- Imagen 15 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 15" class="image image-15" /> -->
    
    <!-- Imagen 16 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 16" class="image image-16" /> -->
    
    <!-- Imagen 17 -->
    <!-- <img src="../assets/section-five/1.webp" alt="imagen 17" class="image image-17" /> -->
    
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
  background-color: #5e6766;
  position: relative;
  width: 100%;
  height: 100vh;
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
  transform: translateX(-50%); /* Asegura que esté centrada horizontalmente */
}

/* Estilos para las imágenes, cada una con un z-index diferente */
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

/* .image-9 {
  top: 290px;
  left: 900px;
  z-index: 10;
}

.image-10 {
  top: 320px;
  left: 100px;
  z-index: 11;
}

.image-11 {
  top: 350px;
  left: 200px;
  z-index: 12;
}

.image-12 {
  top: 380px;
  left: 300px;
  z-index: 13;
}

.image-13 {
  top: 410px;
  left: 400px;
  z-index: 14;
}

.image-14 {
  top: 440px;
  left: 500px;
  z-index: 15;
}

.image-15 {
  top: 470px;
  left: 600px;
  z-index: 16;
}

.image-16 {
  top: 500px;
  left: 700px;
  z-index: 17;
}

.image-17 {
  top: 530px;
  left: 800px;
  z-index: 18;
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
} */
</style>

<template>
  <div class="responsive-section">
    <div class="background-image"></div>
    <div class="image-stack">
      <img src="../assets/section-nine/Cepillo.webp" class="img1" alt="Imagen 1" />
      <img src="../assets/section-nine/Crema dental.webp" class="img2" alt="Imagen 2" />
      <img src="../assets/section-nine/ENjuague.webp" class="img3" alt="Imagen 3" />
      <img src="../assets/section-nine/Sello_1.webp" class="img4" alt="Imagen 4" />
      <!-- Nueva imagen en la esquina superior izquierda -->
      <img src="../assets/section-nine/Logo Periogard.webp" class="img-new" alt="Nueva Imagen" />

      <!-- textos -->
      <img src="../assets/section-nine/Textos_2.webp" class="img-below-new" alt="Imagen Debajo" />

      <img src="../assets/section-nine/Sello condiciones.webp" class="img-below-new-2" alt="Otra Imagen Debajo" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionNine"
};
</script>

<style scoped>
.responsive-section {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url("../assets/section-nine/Fondo.webp");
  object-fit: cover;
  z-index: 1;
}

.image-stack {
  position: relative;
  width: 100%;
  height: 100%;
}

.img1 {
  position: absolute;
  z-index: 4;
  top: 20%; 
  right: 10%; 
  width: 300px; 
}

.img2 {
  position: absolute;
  z-index: 6;
  top: 10%; 
  right: 5%; 
  width: 320px; 
}

.img3 {
  position: absolute;
  z-index: 3;
  top: 60%;  
  right: 20%; 
  width: 280px; 
}

.img4 {
  position: absolute;
  z-index: 5;
  top: 40%;  
  right: 15%; 
  width: 310px; 
}

/* Nueva imagen en la esquina superior izquierda */
.img-new {
  position: absolute;
  top: 0; /* Tocando el borde superior */
  left: 98px; /* Tocando el borde izquierdo */
  width: 100px; /* Ajuste de tamaño */
  z-index: 7; /* Por encima de todas las otras imágenes */
}

/* Nueva imagen debajo de la imagen superior izquierda */
.img-below-new {
  position: absolute;
  top: 120px; /* Ajuste para estar debajo de la imagen superior izquierda */
  left: 75px; /* Alineada con la imagen superior izquierda */
  width: 100px;
  z-index: 6; /* Z-index diferente para que no afecte la imagen superior izquierda */
}

/* Nueva imagen debajo de img-below-new */
.img-below-new-2 {
  position: absolute;
  top: 240px; /* Ajustada para estar debajo de img-below-new */
  left: 225px;
  width: 100px;
  z-index: 9; /* Z-index más alto para que esté encima de todas las demás imágenes */
}


/* Media queries para tablets, priorizando 1180x820 */
@media (max-width: 1180px) and (max-height: 820px) {
  .img1 {
    width: 150px; 
    top: 15%; 
    right: 8%; 
  }
  
  .img2 {
    width: 160px; 
    top: 12%; 
    right: 5%; 
  }

  .img3 {
    width: 140px; 
    top: 55%; 
    right: 18%; 
  }

  .img4 {
    width: 170px; 
    top: 35%; 
    right: 12%; 
  }

  .img-new {
    width: 80px; /* Tamaño ajustado para tablets */
  }

  /* Para resolución de tablet, priorizando 1180x820 */
.img-below-new {
  width: 80px; 
  top: 110px; /* Ajuste de ubicación para tablets */
}

/* Para otras resoluciones de tablet */
.img-below-new {
  width: 518px; /* Ajuste de tamaño para otras resoluciones de tablet */
  top: 216px; /* Ajuste de ubicación para otras resoluciones de tablet */
}

.img-below-new-2 {
  width: 80px;
  top: 230px; /* Ajuste de ubicación para tablets */
}


}

/* Otras resoluciones de tablet */
@media (min-width: 768px) and (max-width: 1024px) and (orientation: portrait),
       (min-width: 1024px) and (max-width: 1366px) and (orientation: landscape),
       (min-width: 800px) and (max-width: 1280px) and (orientation: portrait) {
  .img1 {
    width: 157px;
    top: 6%;
    right: 26%;
  }

  .img2 {
    width: 485px;
    top: 68%;
    right: 11%;
  }

  .img3 {
    width: 427px;
    top: 2%;
    right: -4%;
  }

  .img4 {
    width: 124px;
    top: 80%;
    right: 1%;
  }

  .img-new {
    width: 373px; /* Tamaño ajustado para otras resoluciones de tablet */
  }

  .img-below-new-2 {
  width: 244px;
  top: 388px; /* Ajuste de ubicación para otras resoluciones de tablet */
}

}
</style>

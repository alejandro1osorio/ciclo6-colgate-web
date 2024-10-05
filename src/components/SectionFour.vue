<template>
  <div class="responsive-section">
    <img src="../assets/section-four/Fondo total 12.png" alt="Fondo" class="background-image" />
    <div class="image-container">
      <img src="../assets/section-four/Líneas_1.png" alt="Imagen 1" class="image-one" />
      <img src="../assets/section-four/Crema.png" alt="Imagen 2" class="image-two" />
      <img src="../assets/section-four/Banner.png" alt="Imagen Izquierda" class="image-left" />
      
      <!-- Imagen de fondo del iframe -->
      <div class="iframe-center" @click="showVideo = true"></div>
      
      <!-- Modal para el video -->
      <div v-if="showVideo" class="modal">
        <div class="modal-content">
          <iframe 
            src="https://player.vimeo.com/video/999685698?title=0&byline=0&portrait=0&badge=0&autopause=0&player_id=0&app_id=58479&autoplay=1"
            frameborder="0"
            allow="fullscreen; picture-in-picture; clipboard-write"
            title="Video en Modal"
            class="modal-video"
            allowfullscreen
            muted>
          </iframe>

          <button class="close-button" @click="showVideo = false">Cerrar</button>
        </div>
      </div>

      <!-- Imágenes originales al lado izquierdo del iframe -->
      <img src="../assets/section-four/Engranaje 1_1.png" alt="Imagen 1" class="extra-image image-one-extra" />
      <img src="../assets/section-four/Engranaje 2_1.png" alt="Imagen 2" class="extra-image image-two-extra" />
      <img src="../assets/section-four/Engranaje 3_1.png" alt="Imagen 3" class="extra-image image-three-extra" />

      <!-- Nuevas imágenes centradas sobre las anteriores -->
      <img src="../assets/section-four/Fosfato.png" alt="Nueva Imagen 1" class="extra-image-new image-one-new" />
      <img src="../assets/section-four/Nitrato.png" alt="Nueva Imagen 2" class="extra-image-new image-two-new" />
      <img src="../assets/section-four/Fluoruro de estaño.png" alt="Nueva Imagen 3" class="extra-image-new image-three-new" />

      <!-- Imagen en la esquina superior izquierda -->
      <img src="../assets/section-four/Fluoruro de estaño.png" alt="Logo" class="image-top-left" />

      <!-- Nueva imagen debajo de la imagen 3 -->
      <img src="../assets/section-four/Logo Total SNaP.png" alt="Nueva Imagen Debajo de la Imagen 3" class="image-below-three" />
    </div>
  </div>
</template>

<script>
export default {
  name: "ResponsiveComponent",
  data() {
    return {
      showVideo: false, // Controla la visibilidad del modal
    };
  },
};
</script>

<style scoped>
.responsive-section {
  position: relative;
  width: 100%;
  height: 100vh;
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 1;
}

.image-container {
  position: relative;
  width: 100%;
  height: 100%;
}

.image-one {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 600px;
  z-index: 2;
}

.image-two {
  position: absolute;
  bottom: -13px;
  right: 50px;
  width: 370px;
  z-index: 3;
}

.image-left {
  position: absolute;
  bottom: 20px;
  left: 41px;
  width: 870px;
  z-index: 1;
}

/* Estilo para el iframe que actúa como imagen de fondo */
.iframe-center {
  background: url('../assets/section-four/Botón\ Video.png');
  position: absolute;
  top: 50%;
  left: 50%;
  width: 300px;
  height: 300px;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  z-index: 4;
  cursor: pointer;
}

/* Imágenes adicionales al lado izquierdo del iframe */
.extra-image {
  position: absolute;
  z-index: 5; /* Asegurar que estén por encima de los otros elementos */
}

.extra-image-new {
  position: absolute;
  z-index: 6; /* Encima de las imágenes anteriores */
  transform: translate(-50%, -50%); /* Centramos la nueva imagen sobre la original */
}

/* Ubicación y tamaño personalizado para cada imagen original */
.image-one-extra {
  top: 25%;
  left: 18%;
  width: 194px;
  transform: rotate(56deg);
}

.image-two-extra {
  top: 48%;
  left: 16%;
  width: 192px;
  transform: rotate(236deg);
}

.image-three-extra {
  top: 30%;
  left: 3%;
  width: 200px;
}

/* Nuevas imágenes centradas sobre las anteriores */
.image-one-new {
  top: calc(25% + 97px); /* Centramos la nueva imagen sobre la imagen original */
  left: calc(18% + 97px);
  width: 100px; /* Ajusta el tamaño de la nueva imagen 1 */
}

.image-two-new {
  top: calc(48% + 96px); /* Centramos la nueva imagen sobre la imagen original */
  left: calc(16% + 96px);
  width: 90px; /* Ajusta el tamaño de la nueva imagen 2 */
}

.image-three-new {
  top: calc(30% + 100px); /* Centramos la nueva imagen sobre la imagen original */
  left: calc(3% + 100px);
  width: 110px; /* Ajusta el tamaño de la nueva imagen 3 */
}

/* Imagen en la esquina superior izquierda */
.image-top-left {
  position: absolute;
  top: 94px;
  left: 153px;
  width: 194px; /* Ajusta el tamaño según lo necesites */
  z-index: 10; /* Asegurar que esté encima de todos los elementos */
}

/* Nueva imagen debajo de la imagen 3 */
.image-below-three {
  position: absolute;
  top: calc(32% + 218px); /* Ubica la nueva imagen justo debajo de la imagen 3 */
  left: 46px;
  width: 123px; /* Ajusta el tamaño de la nueva imagen */
  z-index: 7; /* Asegurar que esté encima de las demás imágenes */
}

/* Estilos del modal */
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  position: relative;
  width: 80%;
  max-width: 800px;
  background: #fff;
  padding: 20px;
  border-radius: 10px;
}

.modal-video {
  width: 100%;
  height: 450px;
}

.close-button {
  position: absolute;
  top: 10px;
  right: 10px;
  background: red;
  color: white;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 5px;
}
</style>

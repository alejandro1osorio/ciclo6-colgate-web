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
            src="https://player.vimeo.com/video/1016842689?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479"
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
      <img src="../assets/section-four/Texto.webp" alt="Logo" class="image-top-left" />

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
@keyframes breathe {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.04);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes breathe2 {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes rotateLeft {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(-360deg);
  }
}

@keyframes rotateRight {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

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
  z-index: 0;
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
  z-index: 0;
  animation: breathe 5s ease-in-out infinite;
}

.image-two {
  position: absolute;
  bottom: -13px;
  right: 50px;
  width: 370px;
  z-index: 3;
  animation: breathe2 5s ease-in-out infinite;
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
  background-size: cover;
  position: absolute;
  top: 50%;
  left: 50%;
  width: 220px; /* Tamaño reducido */
  height: 220px; /* Tamaño reducido */
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

.image-three-extra {
  top: 30%;
  left: 6%;
  width: 200px;
  animation: rotateLeft 10s linear infinite; /* Añade la animación de rotación hacia la izquierda */
}

.image-one-extra {
  top: 25%;
  left: 21%;
  width: 194px;
  transform: rotate(56deg);
  animation: rotateRight 8s linear infinite; /* Añade la animación de rotación hacia la derecha */
}

.image-two-extra {
  top: 48%;
  left: 19%;
  width: 192px;
  transform: rotate(236deg);
  animation: rotateRight 8s linear infinite; /* Añade la animación de rotación hacia la derecha */
}

.extra-image-new {
  position: absolute;
  z-index: 6; /* Encima de las imágenes anteriores */
  transform: translate(-50%, -50%); /* Centramos la nueva imagen sobre la original */
}

/* Nuevas imágenes centradas sobre las anteriores */
.image-one-new {
  top: calc(25% + 97px); /* Centramos la nueva imagen sobre la imagen original */
  left: calc(21% + 97px);
  width: 100px; /* Ajusta el tamaño de la nueva imagen 1 */
}

.image-two-new {
  top: calc(48% + 96px); /* Centramos la nueva imagen sobre la imagen original */
  left: calc(19% + 96px);
  width: 90px; /* Ajusta el tamaño de la nueva imagen 2 */
}

.image-three-new {
  top: calc(30% + 100px); /* Centramos la nueva imagen sobre la imagen original */
  left: calc(6% + 100px);
  width: 110px; /* Ajusta el tamaño de la nueva imagen 3 */
}

/* Imagen en la esquina superior izquierda */
.image-top-left {
  position: absolute;
  top: 85px;
  left: 100px;
  width: 397px; /* Ajusta el tamaño según lo necesites */
  z-index: 10; /* Asegurar que esté encima de todos los elementos */
}

/* Nueva imagen debajo de la imagen 3 */
.image-below-three {
  position: absolute;
  top: calc(32% + 218px); /* Ubica la nueva imagen justo debajo de la imagen 3 */
  left: 77px;
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

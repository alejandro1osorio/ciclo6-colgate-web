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
            allowfullscreen>
          </iframe>
          <button class="close-button" @click="showVideo = false">Cerrar</button>
        </div>
      </div>
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

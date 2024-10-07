<template>
  <div class="section-main-container">
    <div class="section-background-red"></div>
    <div class="section-slider-container">
      <img src="@/assets/section-eleven/logo-total2.webp" alt="Logo Total" class="slider-image slider-logo">
      <img src="@/assets/section-eleven/barra-nuevo.png" alt="Barra Nuevo" class="slider-image slider-barra">
      <img src="@/assets/section-eleven/cepillos-solos.png" alt="Cepillos Solos" class="slider-image slider-cepillos animated-breath-bottom-anchor">
      <img src="@/assets/section-eleven/lines.png" alt="Lines" class="slider-image slider-lines animated-breath-left-anchor">
      <img src="@/assets/section-eleven/texto-cerdas.png" alt="Texto Cerdas" class="slider-image slider-texto-cerdas">
      <img v-if="showRedondeadas" src="@/assets/section-eleven/texto-redondeadas.webp" alt="Texto Redondeadas" class="slider-image slider-texto-redondeadas">
      <img v-if="showVideoConicas" src="@/assets/section-eleven/video-c-conicas_1.png" alt="Video Conicas 1" class="slider-image slider-video-conicas-1 animated-fade-in" @click="handleVideoClick('video1')">
      <img v-if="showTextoConicas" src="@/assets/section-eleven/texto-conicas.webp" alt="Texto Conicas" class="slider-image slider-texto-conicas">
      <img v-if="showVideoConicas2" src="@/assets/section-eleven/video-c-conicas_2.png" alt="Video Conicas 2" class="slider-image slider-video-conicas-2 animated-fade-in" @click="handleVideoClick('video2')">
      <img src="@/assets/section-eleven/touch1.png" alt="Touch 1" class="slider-image slider-touch-1" @click="handleTouch1Click">
      <img src="@/assets/section-eleven/touch2.png" alt="Touch 2" class="slider-image slider-touch-2" @click="handleTouch2Click">
      <img src="@/assets/section-eleven/cabeza-cepillo.png" alt="Cabeza Cepillo" class="slider-image slider-cabeza-cepillo">
      <div class="transparent-container"></div>

      <!-- Modal para el video -->
      <div v-if="showVideo" class="modal">
        <div class="modal-content">
          <iframe 
            :src="videoSrc"
            frameborder="0"
            allow="autoplay; fullscreen; picture-in-picture; clipboard-write"
            :title="videoTitle"
            class="modal-video"
            allowfullscreen
            muted>
          </iframe>

          <button class="close-button" @click="showVideo = false">Cerrar</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionEleven',
  data() {
    return {
      showRedondeadas: false,
      showVideoConicas: false,
      showTextoConicas: false,
      showVideoConicas2: false,
      showVideo: false,
      videoSrc: '', // Variable para almacenar la URL del video
      videoTitle: '' // Variable para almacenar el título del video
    };
  },
  methods: {
    handleTouch1Click() {
      this.showRedondeadas = true;
      this.showVideoConicas = true;
    },
    handleTouch2Click() {
      this.showTextoConicas = true;
      this.showVideoConicas2 = true;
    },
    handleVideoClick(videoId) {
      if (videoId === 'video1') {
        this.videoSrc = "https://player.vimeo.com/video/1016835345?title=0&byline=0&portrait=0&badge=0&autopause=0&player_id=0&app_id=58479&autoplay=1";
        this.videoTitle = "Puntas Redondeadas Total 12";
      } else if (videoId === 'video2') {
        this.videoSrc = "https://player.vimeo.com/video/1016835328?title=0&byline=0&portrait=0&badge=0&autopause=0&player_id=0&app_id=58479&autoplay=1";
        this.videoTitle = "Puntas Cónicas Cepillo Total 12";
      }
      this.showVideo = true;
    },
  },
};
</script>

<style scoped>
.section-main-container {
  position: relative;
  width: 1180px;
  height: 820px;
  background: linear-gradient(to bottom right, #ffffff, #d6dcff);
}

.section-background-red {
  position: absolute;
  top: 0;
  left: 0;
  width: 1180px;
  height: 820px;
  background-color: none;
  z-index: 1;
}

.section-slider-container {
  position: absolute;
  top: 0;
  left: 0;
  width: 1180px;
  height: 820px;
  background-color: none;
  overflow-y: auto;
  overflow-x: hidden;
  scrollbar-width: none;
  -ms-overflow-style: none;
  z-index: 2;
}

.section-slider-container::-webkit-scrollbar {
  display: none;
}

.slider-image {
  position: absolute;
  cursor: move;
  resize: both;
  overflow: hidden;
}

.slider-logo {
  top: 100px;
  left: 100px;
  width: 300px;
  z-index: 2;
}

.slider-barra {
  top: 90px;
  left: 980px;
  width: 200px;
}

.slider-cepillos {
  top: 50px;
  left: 500px;
  width: 400px;
  z-index: 2;
}

.slider-lines {
  top: 130px;
  left: 90px;
  width: 1100px;
  z-index: 1;
}

.slider-texto-cerdas {
  top: 500px;
  left: 800px;
  width: 250px;
}

.slider-video-conicas-1 {
  top: 1130px;
  left: 160px;
  width: 160px;
  z-index: 5;
}

.slider-video-conicas-2 {
  top: 1100px;
  left: 890px;
  width: 160px;
  z-index: 5;
}

.slider-texto-redondeadas {
  top: 980px;
  left: 99px;
  width: 400px;
  z-index: 3;
}

.slider-touch-1 {
  top: 1090px;
  left: 460px;
  width: 80px;
  z-index: 4;
}

.slider-touch-2 {
  top: 1029px;
  left: 670px;
  width: 80px;
  z-index: 4;
}

.slider-cabeza-cepillo {
  top: 1050px;
  left: 0px;
  width: 800px;
  z-index: 2;
}

.slider-texto-conicas {
  top: 975px;
  left: 706px;
  width: 400px;
  z-index: 3;
}

.transparent-container {
  height: 200px;
  width: 100%;
  background-color: transparent;
}

@keyframes fadeInBlur {
  0% {
      opacity: 0;
      filter: blur(10px);
  }
  100% {
      opacity: 1;
      filter: blur(0);
  }
}

@keyframes breathAnimationLeftAnchor {
  0%, 100% {
      transform-origin: left;
      transform: scale(1);
  }
  50% {
      transform-origin: left;
      transform: scale(1.05);
  }
}

@keyframes breathAnimationBottomAnchor {
  0%, 100% {
      transform-origin: bottom;
      transform: scale(1);
  }
  50% {
      transform-origin: bottom;
      transform: scale(1.05);
  }
}

.animated-fade-in {
  animation: fadeInBlur 2s ease forwards, breathAnimation 6s ease-in-out infinite;
}

.animated-breath-left-anchor {
  animation: breathAnimationLeftAnchor 6s ease-in-out infinite;
}

.animated-breath-bottom-anchor {
  animation: breathAnimationBottomAnchor 6s ease-in-out infinite;
}

.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
  pointer-events: auto;
}

.modal-content {
  position: relative;
  background: #fff;
  padding: 20px;
  border-radius: 8px;
  max-width: 80%;
  max-height: 80%;
  width: 90%;
  pointer-events: all;
}

.modal-video {
  width: 100%;
  height: 60vh;
}

.close-button {
  position: absolute;
  top: 10px;
  right: 10px;
  background: #333;
  color: #fff;
  border: none;
  padding: 10px;
  cursor: pointer;
}
</style>

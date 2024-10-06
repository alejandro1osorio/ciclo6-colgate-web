<template>
  <div class="section-twelve">
    <!-- Logo Colgate -->
    <div class="logo-colgate">
      <img :src="require('@/assets/section-twelve/logo-cepillo.webp')" alt="Logo Colgate" />
    </div>

    <!-- Imagen de Cepillo -->
    <div class="brush-image" @click="showImages">
      <img :src="require('@/assets/section-twelve/cepillo-periogard1.webp')" alt="Cepillo Periogard" />
    </div>

    <!-- Imagen Nuevo -->
    <transition name="blur-fade">
      <div class="new-image" v-show="isVisibleNuevo">
        <img :src="require('@/assets/section-twelve/nuevo.webp')" alt="Nuevo" />
      </div>
    </transition>

    <!-- Imagen Filamento Cónico -->
    <transition name="blur-bounce">
      <div class="filamento-conico" v-show="isVisibleFilamento">
        <img :src="require('@/assets/section-twelve/filamento-conico.webp')" alt="Filamento Cónico" />
      </div>
    </transition>

    <!-- Imagen Banner 1 -->
    <div class="banner banner1" v-show="isVisibleBanner1">
      <img :src="require('@/assets/section-twelve/banner1.webp')" alt="Banner 1" />
    </div>

    <!-- Imagen Banner 2 -->
    <div class="banner banner2" v-show="isVisibleBanner2">
      <img :src="require('@/assets/section-twelve/banner2.webp')" alt="Banner 2" />
    </div>

    <!-- Imagen Banner 3 -->
    <div class="banner banner3" v-show="isVisibleBanner3">
      <img :src="require('@/assets/section-twelve/banner3.webp')" alt="Banner 3" />
    </div>

    <!-- Imagen Banner 4 -->
    <div class="banner banner4" v-show="isVisibleBanner4">
      <img :src="require('@/assets/section-twelve/banner4.webp')" alt="Banner 4" />
    </div>

    <!-- Imagen Banner 5 -->
    <div class="banner banner5" v-show="isVisibleBanner5">
      <img :src="require('@/assets/section-twelve/banner5.webp')" alt="Banner 5" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionTwelve',
  data() {
    return {
      isVisibleNuevo: false,
      isVisibleFilamento: false,
      isVisibleBanner1: false,
      isVisibleBanner2: false,
      isVisibleBanner3: false,
      isVisibleBanner4: false,
      isVisibleBanner5: false,
    };
  },
  methods: {
    showImages() {
      this.isVisibleNuevo = true;
      setTimeout(() => {
        this.isVisibleFilamento = true;
        this.animateBanners();
      }, 500);
    },
    animateBanners() {
      setTimeout(() => {
        this.isVisibleBanner1 = true;
      }, 500);
      setTimeout(() => {
        this.isVisibleBanner2 = true;
      }, 1500);
      setTimeout(() => {
        this.isVisibleBanner3 = true;
      }, 2500);
      setTimeout(() => {
        this.isVisibleBanner4 = true;
      }, 3500);
      setTimeout(() => {
        this.isVisibleBanner5 = true;
      }, 4500);
    },
  },
};
</script>

<style scoped>
.section-twelve {
  width: 1180px;
  height: 820px;
  position: relative;
  overflow: hidden;
  background-image: url('@/assets/section-twelve/fondo_cepillo_periogard2.webp');
  background-size: cover;
  background-position: center;
}

.logo-colgate {
  position: absolute;
  top: 30px;
  left: 200px;
  z-index: 1;
}

.logo-colgate img {
  width: 250px;
  height: auto;
}

.brush-image {
  position: absolute;
  bottom: 0;
  left: 45%;
  transform: translateX(-50%);
  z-index: 1;
  cursor: pointer;
}

.brush-image img {
  width: 250px;
  height: auto;
}

.new-image {
  position: absolute;
  top: 60px;
  right: 20px;
  z-index: 5;
}

.new-image img {
  width: 200px;
  height: auto;
}

.filamento-conico {
  position: absolute;
  top: 32%;
  right: 200px;
  transform: translateY(-50%);
  z-index: 2;
}

.filamento-conico img {
  width: 250px;
  height: auto;
}

.banner {
  position: absolute;
  z-index: 3;
  opacity: 0;
  transition: all 1.5s ease, filter 1.5s ease;
  animation: fade-blur-in 1.5s ease forwards;
}

@keyframes fade-blur-in {
  0% {
    opacity: 0;
    filter: blur(20px);
    transform: translate(-50%, -50%);
  }
  100% {
    opacity: 1;
    filter: blur(0);
    transform: translate(0, 0);
  }
}

.banner1 {
  top: 350px;
  left: 230px;
}

.banner1 img {
  width: 300px; /* Puedes cambiar este valor para ajustar el tamaño */
  height: auto;
}

.banner2 {
  top: 470px;
  left: 230px;
}

.banner2 img {
  width: 250px; /* Puedes cambiar este valor para ajustar el tamaño */
  height: auto;
}

.banner3 {
  top: 350px;
  right: 240px;
}

.banner3 img {
  width: 280px; /* Puedes cambiar este valor para ajustar el tamaño */
  height: auto;
}

.banner4 {
  top: 470px;
  right: 240px;
}

.banner4 img {
  width: 260px; /* Puedes cambiar este valor para ajustar el tamaño */
  height: auto;
}

.banner5 {
  top: 590px;
  right: 240px;
}

.banner5 img {
  width: 270px; /* Puedes cambiar este valor para ajustar el tamaño */
  height: auto;
}

/* Transiciones */
.blur-fade-enter-active,
.blur-fade-leave-active {
  transition: opacity 1s ease, filter 1s ease;
}
.blur-fade-enter,
.blur-fade-leave-to {
  opacity: 0;
  filter: blur(10px);
}

.blur-bounce-enter-active {
  animation: blur-bounce 0.7s ease;
}

@keyframes blur-bounce {
  0% {
    opacity: 0;
    transform: scale(0.8) translateY(-50%);
    filter: blur(10px);
  }
  50% {
    opacity: 0.5;
    transform: scale(1.1) translateY(-50%);
    filter: blur(5px);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateY(-50%);
    filter: blur(0);
  }
}
</style>

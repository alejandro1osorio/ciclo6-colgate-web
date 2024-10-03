<template>
  <section class="section-one">
    <div class="background-container"></div>

    <!-- Imagen Derecha -->
    <div class="right-image-container animate-right">
      <img src="../assets/section-one/Portada-ciclo-6.1.png" alt="Imagen derecha" class="responsive-image" />
    </div>

    <!-- Imagen Inferior Izquierda -->
    <img src="../assets/section-one/Nube-Portada-ciclo-6.png" alt="Imagen inferior izquierda" class="bimg-responsive animate-bottom" />

    <!-- Texto en la esquina inferior izquierda -->
    <div class="text-container animate-text">
      <p class="responsive-text">
        En sus manos<br />
        está la posibilidad<br />
        de transformar sonrisas<br />
        y mejorar la calidad de vida<br />
        de muchas personas.
      </p>
    </div>

    <!-- Imagen en la esquina superior izquierda -->
    <img src="../assets/section-one/Logo-Colgate.webp" alt="Logo" class="top-left-image animate-top-left" />
  </section>
</template>

<script>
export default {
  name: 'SectionOne',
}
</script>

<style scoped>
@font-face {
  font-family: 'ColgateReady-Regular';
  src: url('../assets/fonts/ColgateReady-Regular.ttf') format('truetype');
}

/* Estructura base */
.section-one {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.background-container {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('../assets/section-one/Fondo-Portada-ciclo-6.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  animation: fade-in 1.5s ease-in-out forwards;
}

/* Animaciones de los elementos */
.animate-right {
  animation: slide-right 1s ease-in-out forwards;
}

.animate-bottom {
  animation: slide-up 1.5s ease-in-out forwards;
}

.animate-text {
  animation: fade-in-text 2s ease-in-out forwards;
}

.animate-top-left {
  animation: bounce-in 2s ease-in-out forwards;
}

/* Imagen derecha */
.right-image-container {
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 30%;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
}

.responsive-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.bimg-responsive {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 95%;
  object-fit: cover;
  z-index: 1;
}

.text-container {
  position: absolute;
  bottom: 50px;
  left: 116px;
  z-index: 2;
  color: #B28236;
}

.responsive-text {
  font-family: 'ColgateReady-Regular', sans-serif;
  font-size: 2.9rem;
  text-align: left;
  margin: 0;
  line-height: 40px;
  margin-bottom: 80px;
}

.top-left-image {
  position: absolute;
  top: 0;
  left: 124px;
  width: 184px;
  height: auto;
  z-index: 3;
  border-bottom-left-radius: 100px;
  border-bottom-right-radius: 100px;
}

/* Animaciones por media query */
@media (max-width: 768px) {
  .responsive-text {
    font-size: 1.2rem;
  }

  .top-left-image {
    width: 80px;
    border-bottom-left-radius: 75px;
    border-bottom-right-radius: 75px;
  }
}

@media (max-width: 480px) {
  .responsive-text {
    font-size: 1rem;
  }

  .top-left-image {
    width: 60px;
    border-bottom-left-radius: 50px;
    border-bottom-right-radius: 50px;
  }
}

@media (min-width: 768px) and (max-width: 1024px),
       (min-width: 1024px) and (max-width: 1366px) {
  .section-one {
    height: 100vh;
  }

  .background-container {
    background-size: cover;
    background-position: center;
  }

  .right-image-container {
    width: 48%;
  }
}

@media (max-width: 1024px) and (max-height: 768px) {
  .right-image-container {
    width: 55%;
  }
}

/* Animations */
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes slide-right {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0);
  }
}

@keyframes slide-up {
  0% {
    transform: translateY(100%);
  }
  100% {
    transform: translateY(0);
  }
}

@keyframes fade-in-text {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes bounce-in {
  0% {
    transform: scale(0.5);
    opacity: 0;
  }
  60% {
    transform: scale(1.1);
    opacity: 1;
  }
  100% {
    transform: scale(1);
  }
}
</style>

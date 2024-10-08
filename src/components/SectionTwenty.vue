<template>
  <div class="container">
    <img src="../assets/section-twenty/logo_colpass.webp" alt="Logo" class="logo">
    <div class="content">
      <div class="left" @click="triggerAnimation">
        <img src="../assets/section-twenty/call_center.webp" alt="Call Center" class="breathing-img">
      </div>
      <div class="right" @click="triggerAnimation">
        <img src="../assets/section-twenty/presencial.webp" alt="Presencial" class="breathing-img">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      animateLogo: false
    };
  },
  methods: {
    triggerAnimation() {
      // Puedes usar esta función si necesitas activar otras animaciones
    }
  }
};
</script>

<style>
  .container {
    width: 100%;
    height: 820px;
    background: url('../assets/section-twenty/fondo.webp') no-repeat center center;
    background-size: cover;
    display: flex;
    flex-direction: column;
    position: relative;
    overflow: hidden; /* Para que las imágenes no se vean fuera del contenedor */
  }

  .logo {
    width: 500px;
    height: auto;
    position: absolute;
    top: 80px;
    left: 50%;
    transform: translateX(-50%);
  }

  .content {
    display: flex;
    height: 100%;
    margin-top: 0;
  }

  .left, .right {
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    position: relative;
  }

  .left img, .right img {
    width: 321.45px;
    height: auto;
    margin-top: 300px;
    position: absolute;
    animation: breathing 3s ease-in-out infinite; /* Animación de respiración */
  }

  .right img {
    width: 308.75px;
    right: 25%;
  }

  /* Animación de respiración */
  @keyframes breathing {
    0%, 100% {
      transform: scale(1); /* Estado inicial y final (sin cambios) */
    }
    50% {
      transform: scale(1.05); /* Aumenta ligeramente el tamaño al 50% del ciclo */
    }
  }
</style>
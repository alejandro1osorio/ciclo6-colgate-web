<template>
  <section class="container-nineteen">
    <img class="image-text" :class="{ animated: animated }" src="../assets/section-nineteen/texto_1.webp" alt="Texto 1" />
  </section>
</template>

<!-- Código restante igual -->


<script>
export default {
  name: "SectionNineteen",
  data() {
    return {
      animated: false, // Control de animación
    };
  },
  mounted() {
    this.createObserver(); // Crea el observer cuando el componente se monta
  },
  methods: {
    createObserver() {
      const options = {
        root: null, // Usa el viewport del navegador
        rootMargin: '0px',
        threshold: 0.5, // Se activará cuando el 50% del contenedor sea visible
      };

      const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
console.log("SectionNineteen is in view");
this.animated = true; // Activa la animación
}

        });
      }, options);

      // Observa el contenedor de la sección
      observer.observe(this.$el);
    },
  },
};
</script>

<style scoped>

@font-face {
  font-family: 'ColgateReady-Regular';
  src: url('../assets/fonts/ColgateReady-Regular.ttf') format('truetype');
}

.container-nineteen {
  width: 1180px;
  height: 820px;
  background-image: url("../assets/section-nineteen/fondo_colgatepass.webp");
  background-size: cover;
  position: relative;
  overflow: hidden;   
  background-repeat: no-repeat;
}

/* Imagen con animaciones */
.image-text {
  position: absolute;
  top: 100px;
  left: 50px;
  width: 40%;
  height: auto;
  opacity: 0;
  transform: rotateX(-90deg);
  transition: opacity 1.5s ease-in-out, transform 1.5s ease-in-out;
}

/* Activar animaciones cuando animated es verdadero */
.image-text.animated {
  opacity: 1;
  transform: rotateX(0deg);
}
</style>
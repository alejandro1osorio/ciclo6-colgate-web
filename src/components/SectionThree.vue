<template>
  <section ref="section">
    <!-- Imagen Izquierda -->
    <img
      src="../assets/section-three/Logo Total.png"
      alt="Imagen Izquierda"
      class="imagen-izquierda animate-on-scroll"
    />

    <div class="imagenes-abajo animate-on-scroll">
      <!-- Contenedor de las imágenes 1, 2, y 3 -->
      <div class="contenedor-izquierdo" style="margin-left: 60px;">
        <div class="imagen-superior" style="position: relative;">
          <img
            src="../assets/section-three/círculo.webp"
            alt="Imagen 1"
            class="imagen-rotacion"
          />
          <img
            src="../assets/section-three/Estaño.webp"
            alt="Imagen Superior 1"
            class="imagen-superior-1 animate-on-scroll"
          />
          <!-- Nueva imagen debajo de la imagen 1 -->
          <img
            src="../assets/section-three/Texto Estaño.webp"
            alt="Imagen Inferior 1"
            class="imagen-inferior-1 animate-on-scroll"
          />
        </div>
        <img src="../assets/section-three/+.webp" alt="Imagen 2" class="animate-on-scroll" />
        <div class="imagen-superior" style="position: relative;">
          <img
            src="../assets/section-three/círculo.webp"
            alt="Imagen 3"
            class="imagen-rotacion"
          />
          <img
            src="../assets/section-three/Fluoruro_1.webp"
            alt="Imagen Superior 2"
            class="imagen-superior-2 animate-on-scroll"
          />
          <!-- Nueva imagen debajo de la imagen 3 -->
          <img
            src="../assets/section-three/Texto Fluoruro.webp"
            alt="Imagen Inferior 2"
            class="imagen-inferior-2 animate-on-scroll"
          />
        </div>
      </div>

      <img
        src="../assets/section-three/Textos2.webp"
        alt="Subtítulo Intermedio"
        class="subtititulo-intermedio animate-on-scroll"
      />

      <!-- Contenedor de las imágenes 4 y 5 con sus imágenes inferiores -->
      <div class="contenedor-derecho" style="margin-right: 60px;">
        <div class="contenedor-imagen4 animate-on-scroll">
          <img
            src="../assets/section-three/1formula-a.webp"
            alt="Imagen 4"
            class="imagen-4"
          />
          <img
            src="../assets/section-three/1formula-c.webp"
            alt="Otra Imagen Debajo de 4"
            class="imagen-debajo-4"
          />
          <img src="../assets/section-three/1formula-b.webp" alt="Llave 1" class="llave1 animate-on-scroll" />
        </div>

        <div class="contenedor-imagen5 animate-on-scroll">
          <img
            src="../assets/section-three/2formula-a.webp"
            alt="Imagen 5"
            class="imagen-5"
          />
          <img
            src="../assets/section-three/2formula-c.webp"
            alt="Otra Imagen Debajo de 5"
            class="imagen-debajo-5"
          />
          <img src="../assets/section-three/2formula-b.webp" alt="Llave 2" class="llave2 animate-on-scroll" />
        </div>
      </div>
    </div>

    <!-- Imagen adicional ubicada en la esquina inferior izquierda -->
    <img
      src="../assets/section-three/Textos_1.webp"
      alt="Imagen Esquina Inferior Izquierda"
      class="imagen-esquina animate-on-scroll"
    />

    <!-- Imagenes en la esquina inferior derecha -->
    <img
      src="../assets/section-three/Textos2.webp"
      alt="Imagen Esquina Inferior Derecha 1"
      class="imagen-esquina-derecha-arriba animate-on-scroll"
    />
    <img
      src="../assets/section-three/Logo Total SNaP.webp"
      alt="Imagen Esquina Inferior Derecha 2"
      class="imagen-esquina-derecha-abajo animate-on-scroll"
    />
  </section>
</template>


<script>
export default {
  name: "SectionThree",
  mounted() {
    const options = {
      root: null, // Viewport
      threshold: 0.1, // Trigger when 10% of the element is visible
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
        }
      });
    }, options);

    // Observa todos los elementos con la clase 'animate-on-scroll'
    const elements = this.$refs.section.querySelectorAll(".animate-on-scroll");
    elements.forEach((el) => observer.observe(el));
  },
};
</script>


<style scoped>
@keyframes rotate-circle {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.imagen-rotacion {
  animation: rotate-circle 2s linear infinite;
}

.animate-on-scroll {
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}

.animate-on-scroll.visible {
  opacity: 1;
}

section {
  position: relative;
  margin-top: 20px;
  width: 100%;
  height: calc(100vh - 40px);
  overflow: hidden;
}

.imagen-izquierda {
  width: 350px;
  height: auto;
  position: absolute;
  top: 20px;
  left: 20px;
}

.imagenes-abajo {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: absolute;
  bottom: 40px;
  top: 40px;
  width: 100%;
}

.contenedor-izquierdo,
.contenedor-derecho {
  display: flex;
  align-items: center;
}

.contenedor-izquierdo img,
.contenedor-derecho img {
  margin-left: 10px;
}

/* Nueva clase para el contenedor de las imágenes superpuestas */
.imagen-superior {
  position: relative;
  display: inline-block;
}

/* Clases para las imágenes que se superponen encima de las imágenes 1 y 3 */
.imagen-superior-1,
.imagen-superior-2 {
  position: absolute;
  top: 50%; /* Centrar verticalmente */
  left: 50%; /* Centrar horizontalmente */
  transform: translate(-50%, -50%); /* Ajusta para centrar completamente */
  width: 170px; /* Ajusta el tamaño si es necesario */
  height: auto;
  z-index: 1; /* Para asegurarse de que esté encima de las imágenes base */
}

/* Clases para las imágenes que se colocan debajo de las imágenes 1 y 3 */
.imagen-inferior-1,
.imagen-inferior-2 {
  position: absolute;
  top: 100%; /* Coloca la imagen debajo de la imagen base */
  left: 50%; /* Centrar horizontalmente */
  transform: translate(-50%, 10px); /* Ajusta para posicionar debajo */
  width: 196px; /* Ajusta el tamaño según sea necesario */
  height: auto;
  z-index: 1; /* Para asegurarse de que esté debajo de las imágenes base */
}

.subtititulo-intermedio {
  position: absolute;
  left: 871px;
  top: 166px;
  width: 190px;
  z-index: 4;
}

/* Clases para las imágenes debajo de las imágenes 4 y 5 */
.contenedor-imagen4,
.contenedor-imagen5 {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.imagen-debajo-4,
.imagen-debajo-5 {
  margin-top: 10px;
  width: 150px; /* Ajusta el tamaño según sea necesario */
  height: auto;
  z-index: 1;
}

.llave1 {
  position: absolute;
  top: 394px;
  left: 766px;
  width: 60px;
  z-index: 3;
}

.llave2 {
  position: absolute;
  top: 404px;
  left: 1091px;
  width: 54px;
  z-index: 3;
}

/* Clase para la imagen adicional ubicada en la esquina inferior izquierda */
.imagen-esquina {
  position: absolute;
  bottom: 66px;
  left: 290px;
  width: 250px; /* Ajusta el tamaño según sea necesario */
  height: auto;
  z-index: 1; /* Asegura que se superponga correctamente */
}

/* Clases para las imágenes en la esquina inferior derecha */
.imagen-esquina-derecha-arriba {
  position: absolute;
  bottom: 140px; /* Ajusta para posicionar la imagen arriba */
  right: 56px;
  width: 250px; /* Ajusta el tamaño según sea necesario */
  height: auto;
  z-index: 1; /* Asegura que se superponga correctamente */
}

.imagen-esquina-derecha-abajo {
  position: absolute;
  bottom: 46px; /* Ajusta para posicionar la imagen abajo */
  right: 100px;
  width: 130px; /* Ajusta el tamaño según sea necesario */
  height: auto;
  z-index: 1; /* Asegura que se superponga correctamente */
}

/* Estilos responsivos para tablet */
@media (max-width: 1024px) {
  .contenedor-izquierdo {
    margin-left: 20px; /* Controla la distancia del borde izquierdo */
  }

  .contenedor-derecho {
    margin-right: 60px; /* Añade suficiente espacio del lado derecho */
    display: flex;
    flex-direction: row;
    gap: 10px; /* Espacio entre las imágenes */
  }

  .imagen-esquina {
    width: 200px; /* Ajusta el tamaño en dispositivos más pequeños */
  }

  .imagen-esquina-derecha-arriba,
  .imagen-esquina-derecha-abajo {
    width: 200px; /* Ajusta el tamaño en dispositivos más pequeños */
  }

  .imagen-debajo-4,
  .imagen-debajo-5 {
    width: 120px; /* Ajusta el tamaño en dispositivos más pequeños */
  }
}
</style>
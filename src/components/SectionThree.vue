<template>
  <section>
    <!-- Imagen Izquierda -->
    <img
      src="../assets/section-three/Logo Total.png"
      alt="Imagen Izquierda"
      class="imagen-izquierda"
    />

    <div class="imagenes-abajo">
      <!-- Contenedor de las imágenes 1, 2, y 3 -->
      <div class="contenedor-izquierdo" style="margin-left: 60px;">
        <div class="imagen-superior" style="position: relative;">
          <img src="../assets/section-three/círculo.webp" alt="Imagen 1" />
          <img
            src="../assets/section-three/Estaño.webp"
            alt="Imagen Superior 1"
            class="imagen-superior-1"
          />
          <!-- Nueva imagen debajo de la imagen 1 -->
          <img
            src="../assets/section-three/Texto Estaño.webp"
            alt="Imagen Inferior 1"
            class="imagen-inferior-1"
          />
        </div>
        <img src="../assets/section-three/+.webp" alt="Imagen 2" />
        <div class="imagen-superior" style="position: relative;">
          <img src="../assets/section-three/círculo.webp" alt="Imagen 3" />
          <img
            src="../assets/section-three/Fluoruro_1.webp"
            alt="Imagen Superior 2"
            class="imagen-superior-2"
          />
          <!-- Nueva imagen debajo de la imagen 3 -->
          <img
            src="../assets/section-three/Texto Fluoruro.webp"
            alt="Imagen Inferior 2"
            class="imagen-inferior-2"
          />
        </div>
      </div>

      <!-- Contenedor de las imágenes 4 y 5 -->
      <div class="contenedor-derecho" style="margin-right: 60px;">
        <img
          src="../assets/section-three/Fómula Bio Activo.webp"
          alt="Imagen 4"
          style="margin-right: 19px;"
        />
        <img src="../assets/section-three/Fórmula No Bio Activo.webp" alt="Imagen 5" />
      </div>
    </div>

    <!-- Imagen adicional ubicada en la esquina inferior izquierda -->
    <img
      src="../assets/section-three/Textos_1.webp"
      alt="Imagen Esquina Inferior Izquierda"
      class="imagen-esquina"
    />

    <!-- Imagenes en la esquina inferior derecha -->
    <img
      src="../assets/section-three/Textos2.webp"
      alt="Imagen Esquina Inferior Derecha 1"
      class="imagen-esquina-derecha-arriba"
    />
    <img
      src="../assets/section-three/Logo Total SNaP.webp"
      alt="Imagen Esquina Inferior Derecha 2"
      class="imagen-esquina-derecha-abajo"
    />
  </section>
</template>

<script>
export default {
  name: "SectionThree",
};
</script>

<style scoped>
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
}
</style>

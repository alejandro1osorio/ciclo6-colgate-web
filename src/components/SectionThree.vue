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
        </div>
        <img src="../assets/section-three/+.webp" alt="Imagen 2" />
        <div class="imagen-superior" style="position: relative;">
          <img src="../assets/section-three/círculo.webp" alt="Imagen 3" />
          <img
            src="../assets/section-three/Fluoruro_1.webp"
            alt="Imagen Superior 2"
            class="imagen-superior-2"
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
}
</style>

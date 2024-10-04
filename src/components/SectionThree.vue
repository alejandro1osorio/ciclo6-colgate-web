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
      <div class="contenedor-izquierdo" style="margin-left: 40px;">
        <img src="../assets/section-three/círculo.webp" alt="Imagen 1" />
        <img src="../assets/section-three/+.webp" alt="Imagen 2" />
        <img src="../assets/section-three/círculo.webp" alt="Imagen 3" />
      </div>

      <!-- Contenedor de las imágenes 4 y 5 -->
      <div class="contenedor-derecho" style="margin-right: 40px;">
        <img
          src="../assets/section-three/Fómula Bio Activo.webp"
          alt="Imagen 4"
        />
        <img
          src="../assets/section-three/Fórmula No Bio Activo.webp"
          alt="Imagen 5"
        />
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

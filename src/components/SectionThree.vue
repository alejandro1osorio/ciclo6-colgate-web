<template>
  <section>
    <!-- Imagen Izquierda -->
    <img
      src="../assets/section-three/Logo Total.png"
      alt="Imagen Izquierda"
      class="imagen-izquierda"
    />

    <div class="imagenes-abajo">
      <img src="../assets/section-three/círculo.webp" alt="Imagen 1" />
      <img src="../assets/section-three/+.webp" alt="Imagen 2" />
      <img src="../assets/section-three/círculo.webp" alt="Imagen 3" />
      <img src="../assets/section-three/Fómula Bio Activo.webp" alt="Imagen 4" />
      <img src="../assets/section-three/Fórmula No Bio Activo.webp" alt="Imagen 5" />
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
  margin-top: 20px; /* Ajusta el margen superior según sea necesario */
  width: 100%; /* O ajusta a un valor específico, como '800px' */
  height: calc(100vh - 40px); /* Aumenta la altura de la sección para permitir más espacio */
  overflow: hidden; /* Para evitar que las imágenes sobresalgan */
}

.imagen-izquierda {
  width: 350px;
  height: auto;
  position: absolute;
  top: 20px; /* Margen superior */
  left: 20px; /* Margen izquierdo */
}

.imagenes-abajo {
  display: flex; /* Usar flexbox para alinear las imágenes */
  align-items: center; /* Alinea verticalmente las imágenes al centro */
  justify-content: center; /* Centra el contenedor horizontalmente */
  position: absolute; /* Asegúrate de que el contenedor esté posicionado respecto a la sección */
  bottom: 40px; /* Espacio desde el borde inferior */
  top: 40px; /* Espacio desde el borde superior */
  width: 100%; /* Asegúrate de que ocupe todo el ancho de la sección */
  margin: auto; /* Centra el contenedor verticalmente */
}

.imagenes-abajo img {
  margin-left: 10px; /* Espacio entre imágenes */
}
</style>

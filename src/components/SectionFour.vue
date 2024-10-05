<template>
  <div class="responsive-section">
    <img src="../assets/section-four/Fondo total 12.png" alt="Fondo" class="background-image" />
    <div class="image-container">
      <img src="../assets/section-four/Líneas_1.png" alt="Imagen 1" class="image-one" />
      <img src="../assets/section-four/Crema.png" alt="Imagen 2" class="image-two" />
      <img src="../assets/section-four/Banner.png" alt="Imagen Izquierda" class="image-left" />
    </div>
  </div>
</template>

<script>
export default {
  name: "ResponsiveComponent",
};
</script>

<style scoped>
.responsive-section {
  position: relative;
  width: 100%;
  height: 100vh; /* Ocupar todo el alto de la pantalla */
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover; /* Asegurar que la imagen de fondo cubra todo el espacio */
  z-index: 1;
}

.image-container {
  position: relative;
  width: 100%;
  height: 100%; /* Permite que las imágenes estén dentro de toda la sección */
}

.image-one {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 600px; /* Ajusta el tamaño de la imagen 1 de forma individual */
  z-index: 2; /* Debajo de la imagen 2 */
}

.image-two {
  position: absolute;
  bottom: -13px; /* Ajusta la distancia desde el borde inferior */
  right: 50px; /* Ajusta la distancia desde el borde derecho */
  width: 370px; /* Tamaño aumentado de la imagen 2 */
  z-index: 3; /* Encima de la imagen 1 */
}

.image-left {
  position: absolute;
  bottom: 20px;
  left: 41px; /* Ubica la imagen en la esquina inferior izquierda */
  width: 870px; /* Ajusta el tamaño de la imagen izquierda */
  z-index: 1; /* Debajo de la imagen 2 */
}
</style>

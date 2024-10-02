<template>
    <section class="section-one">
        a
    </section>
</template>

<script>
export default {
    name: 'SectionOne',
}
</script>

<style>
.section-one {
    height: 100vh; /* Altura de la sección para ocupar toda la vista */
    background-image: url('../assets/Fondo-Portada-ciclo-6.png'); /* Cambia esta URL a la ruta de tu imagen */
    background-size: cover; /* La imagen cubre toda la sección */
    background-position: center; /* Centra la imagen */
    background-repeat: no-repeat; /* No repetir la imagen */
}

/* Estilos específicos para tabletas */
@media (max-width: 1024px) {
    .section-one {
        height: 80vh; /* Ajustar altura en tabletas, si es necesario */
    }
}

/* Estilos específicos para dispositivos móviles */
@media (max-width: 768px) {
    .section-one {
        height: 60vh; /* Ajustar altura en móviles, si es necesario */
    }
}
</style>
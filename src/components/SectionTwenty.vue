<template>
  <div class="container">
        <img src="../assets/section-twenty/logo_colpass.webp" alt="Logo" class="logo">
        <div class="content">
            <div class="left">
                <img src="../assets/section-twenty/call_center.webp" alt="Call Center">
            </div>
            <div class="right">
                <img src="../assets/section-twenty/presencial.webp" alt="Presencial">
            </div>
        </div>
    </div>
</template>

<script>
export default {
  
}
</script>

<style>
/* body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 200vh; 
            background-color: #f0f0f0;
        } */

        .container {
            width: 1180px;
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
            opacity: 0; /* Comienza con opacidad 0 */
            filter: blur(70px); /* Comienza con desenfoque de 70px */
            transition: opacity 1s ease-out, filter 1s ease-out; /* Transiciones suaves para opacidad y desenfoque */
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

        .left img {
            width: 321.45px;
            height: auto;
            margin-top: 300px;
            position: absolute;
            left: -50%;
            transition: transform 1s ease-out;
        }

        .right img {
            width: 308.75px;
            height: auto;
            margin-top: 300px;
            position: absolute;
            right: -50%;
            transition: transform 1s ease-out;
        }

        /* Scroll trigger for parallax images */
        .scrolled .left img {
            transform: translateX(150%);
        }

        .scrolled .right img {
            transform: translateX(-150%);
        }

        /* Scroll trigger for logo animation */
        .scrolled .logo {
            opacity: 1; /* Cambia opacidad a 100% */
            filter: blur(0); /* El desenfoque se reduce a 0 */
        }
</style>
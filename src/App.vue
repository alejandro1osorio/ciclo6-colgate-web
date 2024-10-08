<template>
  <div v-if="appVisible" id="app">
    <img src="../src/assets/ciclo 6.png" alt="Header Image" class="header-image colgate" /> <!-- Imagen centrada -->
    <div v-if="currentView === 'home'" class="button-container botones">
      <button @click="showSection('perioCirugia', 'perio/cirugia/implantes/prosto')" class="button-perio">PERIO CIRUGÍA IMPLANTES PROSTO</button>
      <button @click="showSection('orthoOdontoped', 'ortho/odontoped')" class="button-ortho">ORTHO ODONTOPED</button>
      <button @click="showSection('generalEndoEstetica', 'general/endodoncia/estetica')" class="button-general">GENERAL ENDODONCIA ESTETICA</button>
    </div>
  </div>
  <div v-else>
    <!-- Cambio del botón por un SVG -->
    <img @click="showHome" class="home-button" v-show="currentView !== 'home'" src="../src/assets/home_ciclo6.svg" alt="Home Button" />
    <div v-for="section in currentSections" :key="section">
      <component :is="section" />
    </div>
  </div>
</template>

<script>
import SectionOne from './components/SectionOne.vue';
import SectionTwo from './components/SectionTwo.vue';
import SectionThree from './components/SectionThree.vue';
import SectionFour from './components/SectionFour.vue';
import SectionFive from './components/SectionFive.vue';
import SectionEight from './components/SectionEight.vue';
import SectionNine from './components/SectionNine.vue';
import SectionEleven from './components/SectionEleven.vue';
import SectionTwelve from './components/SectionTwelve.vue';
import SectionThirteen from './components/SectionThirteen.vue';
import SectionFourteen from './components/SectionFourteen.vue';
import SectionFifteen from './components/SectionFifteen.vue';
import SectionSixteen from './components/SectionSixteen.vue';
import SectionSeventeen from './components/SectionSeventeen.vue';
import SectionEighteen from './components/SectionEighteen.vue';
import SectionNineteen from './components/SectionNineteen.vue';
import SectionTwenty from './components/SectionTwenty.vue';
import SectionFinal from './components/SectionFinal.vue';

export default {
  name: 'App',
  components: {
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFour,
    SectionFive,
    SectionEight,
    SectionNine,
    SectionEleven,
    SectionTwelve,
    SectionThirteen,
    SectionFourteen,
    SectionFifteen,
    SectionSixteen,
    SectionSeventeen,
    SectionEighteen,
    SectionNineteen,
    SectionTwenty,
    SectionFinal,
  },
  data() {
    return {
      currentView: 'home',
      currentSections: [],
      appVisible: true, // Nueva variable para controlar la visibilidad del contenedor principal
    };
  },
  methods: {
    showSection(sectionGroup, slug) {
      this.appVisible = false; // Ocultar el componente App.vue
      switch (sectionGroup) {
        case 'perioCirugia':
          this.currentSections = [
            'SectionOne',
            'SectionTwo',
            'SectionThree',
            'SectionFour',
            'SectionFive',
            'SectionEleven',
            'SectionEight',
            'SectionNine',
            'SectionTwelve',
            'SectionThirteen',
            'SectionFourteen',
            'SectionSeventeen',
            'SectionEighteen',
            'SectionNineteen',
            'SectionTwenty',
            'SectionFinal',
          ];
          break;
        case 'orthoOdontoped':
          this.currentSections = [
            'SectionOne',
            'SectionTwo',
            'SectionThree',
            'SectionFour',
            'SectionFive',
            'SectionEleven',
            'SectionEight',
            'SectionFifteen',
            'SectionSixteen',
            'SectionFourteen',
            'SectionNineteen',
            'SectionTwenty',
            'SectionFinal',
          ];
          break;
        case 'generalEndoEstetica':
          this.currentSections = [
            'SectionOne',
            'SectionTwo',
            'SectionThree',
            'SectionFour',
            'SectionFive',
            'SectionEleven',
            'SectionEight',
            'SectionSeventeen',
            'SectionEighteen',
            'SectionNine',
            'SectionFourteen',
            'SectionNineteen',
            'SectionTwenty',
            'SectionFinal',
          ];
          break;
      }
      this.currentView = 'sections';
      window.history.pushState(null, '', `/${slug}`);
    },
    showHome() {
      this.appVisible = true; // Volver a mostrar el componente App.vue
      this.currentView = 'home';
      this.currentSections = [];
      window.history.pushState(null, '', '/');
    },
    sectionExists(section) {
      return this.$options.components.hasOwnProperty(section);
    },
    handlePopState() {
      if (window.location.pathname === '/') {
        this.showHome();
      }
    },
  },
  mounted() {
    window.addEventListener('popstate', this.handlePopState);
  },
  beforeDestroy() {
    window.removeEventListener('popstate', this.handlePopState);
  },
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
}

.header-image {
  display: block;
  margin: 10px auto;
  width: 70%;
  max-width: 500px; /* Ajuste del tamaño de la imagen */
}

.colgate {
  margin-top: 100px;
  width: 380px;
}

.button-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  height: calc(100vh - 486px); /* Ajuste para subir los botones más hacia arriba */
}

button {
  margin: 10px;
  padding: 15px 30px;
  font-size: 20px;
  cursor: pointer;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.3); /* Sombra para los botones */
  border: none;
  border-radius: 40px;
  transition: all 0.3s ease;
}

button:hover {
  transform: translateY(-3px);
  box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.35);
}

/* Colores de los botones */
.button-perio {
  background-color: #287db2; /* Color rojo-naranja */
  color: white;
}

.button-ortho {
  background-color: #56ad96; /* Color verde */
  color: white;
}

.button-general {
  background-color: #bea43F; /* Color azul */
  color: white;
}

/* Estilos para el botón de home usando el SVG en la esquina inferior derecha */
.home-button {
  position: fixed;
  bottom: 20px; /* Posiciona en la parte inferior */
  right: 20px; /* Posiciona en la parte derecha */
  width: 40px; /* Ajusta el tamaño del SVG */
  height: 40px;
  cursor: pointer;
  z-index: 100;
}
</style>
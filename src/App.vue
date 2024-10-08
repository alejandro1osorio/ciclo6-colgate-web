<template>
  <div id="app">
    <div v-if="currentView === 'home'" class="button-container">
      <button @click="showSection('perioCirugia', 'perio/cirugia/implantes/prosto')">PERIO CIRUGÍA IMPLANTES PROSTO</button>
      <button @click="showSection('orthoOdontoped', 'ortho/odontoped')">ORTHO ODONTOPED</button>
      <button @click="showSection('generalEndoEstetica', 'general/endodoncia/estetica')">GENERAL ENDODONCIA ESTETICA</button>
    </div>
    <div v-else>
      <button @click="showHome" class="home-button" v-show="currentView !== 'home'">Volver al Home</button>
      <div v-for="section in currentSections" :key="section">
        <component :is="section" />
      </div>
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
    };
  },
  methods: {
    showSection(sectionGroup, slug) {
      switch (sectionGroup) {
        case 'perioCirugia':
          this.currentSections = [
            'SectionOne',
            'SectionTwo',
            'SectionThree',
            'SectionFour',
            'SectionFive',
            'SectionEleven',
          ];
          break;
        case 'orthoOdontoped':
          this.currentSections = [
            'SectionEight',
            'SectionNine',
            'SectionTwelve',
            'SectionThirteen',
            'SectionFourteen',
            'SectionFifteen',
          ];
          break;
        case 'generalEndoEstetica':
          this.currentSections = [
            'SectionSixteen',
            'SectionSeventeen',
            'SectionEighteen',
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

.button-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

button {
  margin: 10px;
  padding: 15px 30px;
  font-size: 16px;
  cursor: pointer;
}

.home-button {
  position: fixed;
  top: 20px;
  left: 20px;
  padding: 10px 20px;
  font-size: 14px;
  cursor: pointer;
  z-index: 100;
}
</style>
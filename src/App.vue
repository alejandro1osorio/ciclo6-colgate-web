<template>
  <div id="app">
    <!-- <Header /> -->
    <SectionOne />
    <SectionTwo />
    <SectionThree />
    <SectionFour />
    <SectionEight />
    <SectionNine />
    <Hero />

    <SectionFourteen />
    <SectionFifteen />
    <SectionSeventeen />
    <SectionEighteen />
    <SectionNineteen />
    <SectionTwenty />
    <Features />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import SectionOne from './components/SectionOne.vue';
import SectionTwo from './components/SectionTwo.vue';
import SectionThree from './components/SectionThree.vue';
import SectionFour from './components/SectionFour.vue';
import SectionEight from './components/SectionEight.vue';
import SectionNine from './components/SectionNine.vue';
import Hero from './components/Hero.vue';
import SectionFourteen from './components/SectionFourteen.vue';
import SectionFifteen from './components/SectionFifteen.vue';
import SectionSeventeen from './components/SectionSeventeen.vue';
import SectionEighteen from './components/SectionEighteen.vue';
import SectionNineteen from './components/SectionNineteen.vue';
import SectionTwenty from './components/SectionTwenty.vue';
import Features from './components/Features.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFour,
    SectionEight,
    SectionNine,
    Hero,
    SectionFourteen,
    SectionFifteen,
    SectionSeventeen,
    SectionEighteen,
    SectionNineteen,
    SectionTwenty,
    Features,
    Footer,
  },
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
}
</style>

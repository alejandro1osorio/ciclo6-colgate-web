<template>
  <div id="app">
    <!-- <Header /> -->
    <SectionOne />
    <SectionTwo />
    <Hero />
    <Features />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import SectionOne from './components/SectionOne.vue';
import SectionTwo from './components/SectionTwo.vue';
import Hero from './components/Hero.vue';
import Features from './components/Features.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    SectionOne,
    SectionTwo,
    Hero,
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

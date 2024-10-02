<template>
    <section class="features">
      <div class="feature" v-for="(feature, index) in features" :key="index">
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.description }}</p>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Features',
    data() {
      return {
        features: [
          { title: 'Feature 1', description: 'Amazing feature description' },
          { title: 'Feature 2', description: 'Another great feature' },
          { title: 'Feature 3', description: 'More awesomeness here' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .features {
    display: flex;
    justify-content: space-around;
    padding: 3rem;
    background-color: #fff;
  }
  .feature {
    text-align: center;
    max-width: 200px;
  }
  </style>
  
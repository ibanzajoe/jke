<template>
  <div class="hero-index-grid">
    <hero-title class="hero-title" />
    <div class="hero-image">
      <hero-background />

    </div>
    <div class="hero-content">
      <div class="hero-content-heading">
        WELCOME TO HAIR BY JKE
      </div>
      <div class="hero-content-subheading mt-5 mb-3">
        Our expert stylists will help you shine!
      </div>
      <div class="hero-content-button-container mt-5">
        <v-btn outlined class="book-button">
          BOOK ONLINE
        </v-btn>
      </div>
    </div>
  </div>
</template>

<script>
  import heroTitle from './hero-title'
  import heroBackground from './hero-background'

  export default {
    name: "index",
    components: {
      heroTitle, heroBackground
    },
  }
</script>

<style scoped>

  .hero-content-heading, .hero-content-subheading, .hero-content-button-container {
    text-align: center;
  }

  .hero-index-grid {
    display: grid;
    grid-template-rows: auto auto auto;
  }
  .hero-content {
    display: block;
    max-width: 1280px;
    margin: 0 auto;
    padding: 40px 20px;
  }
</style>

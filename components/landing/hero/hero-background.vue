<template>
  <div class="hero-background">
    <div class="hero-background-block">
      <div class="hero-background-color" />
      <div class="hero-background-splash-text">
        Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE
      </div>
    </div>

    <div class="hero-image-container">
      <div class="hero-image-box">
        <div class="hero-image" />
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "hero-background"
  }
</script>

<style scoped>


  /*temporary styles*/

  .hero-background {
    position: relative;
  }

  .hero-background-block {
    position: absolute;
    width: 100%;
    z-index: 2;
    overflow: hidden;
  }

  .hero-background-color {
    background-color: rgb(95, 11, 53);
    height: 615px;
    width: 100%;
    opacity: 0.06;
  }

  .hero-background-splash-text {
    position: absolute;
    transform: rotate(-15deg);
    font-size: 140pt;
    color: rgb(95, 11, 53);
    overflow-wrap: break-word;
    word-wrap: break-word;
    text-align: center;
    font-family: 'Yellowtail';
    top: -200px;
    width: 1500px;
    bottom: 0;
    right: 0;
    opacity: 0.06;
    font-weight: 700;
  }

  .hero-image-container {
    position: relative;
    z-index: 3;
    max-width: 984px;
    width: 100%;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    padding-top: 40px;
    padding-left: 2rem;
    padding-right: 2rem;
  }

  .hero-image-box {
    width: 600px;
    height: 600px;
    padding: 1.5rem;
    background-color: #fff;
    box-shadow: 0 2px 6px 4px rgba(0,0,0,0.1);
  }

  .hero-image {
    width: 100%;
    height: 100%;
    background-image: url('./hero-image.webp');
    background-position: center;
    background-size: 135%;
  }

  @media screen and (max-width: 700px) {
    .hero-background-color {
      height: 280px;
    }

    .hero-background-splash-text {
      font-size: 60pt;
    }

    .hero-image-box {
      width: 280px;
      height: 280px;
    }
  }
</style>

<template>
  <div @click="$emit('switch')" class="booking-app">
    <img src="./screenshot.png" />
  </div>
</template>

<script>
  export default {
    name: "booking-app"
  }
</script>

<style scoped>

  .booking-app img {
    height: 100%;
    width: 100%;
  }
</style>

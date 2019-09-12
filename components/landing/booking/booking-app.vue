<template>
  <div @click="$emit('switch')" class="booking-app">
    <!-- Calendly inline widget begin -->
    <div class="calendly-inline-widget" data-url="https://calendly.com/joebanez/office-scheduler" style="min-width:320px;height:630px;"></div>
    <script type="text/javascript" src="https://assets.calendly.com/assets/external/widget.js"></script>
    <!-- Calendly inline widget end -->
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

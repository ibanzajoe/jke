<template>
  <div class="main-grid">
    <div class="grid-hero">
      <hero />
    </div>
    <div class="grid-services">
      <divider />

      <services />

    </div>
    <div class="grid-booking">

    </div>
    <div class="grid-style">

    </div>
    <div class="grid-contact">

    </div>
    <div class="grid-footer">

    </div>
  </div>
</template>

<script>
import hero from '~/components/landing/hero'
import divider from '~/components/divider'
import services from '~/components/landing/services'

export default {
  components: {
    hero,divider, services
  }
}
</script>

<style scoped>
  .main-grid {
    max-width: 1440px;
    margin: 0 auto;
  }
</style>

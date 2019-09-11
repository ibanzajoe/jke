<template>
  <div class="services-component" >
    <services-list v-for="(service, index) in services"
                   :key="index"
                   :service="service" />
  </div>
</template>

<script>
  import servicesList from './services-list'
  export default {
    name: "services-index",
    props: {
      services: {
        type: Array,
        default: () => []
      }
    },
    components: {
      servicesList
    }
  }
</script>

<style scoped>

</style>

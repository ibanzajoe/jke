<template>
  <div class="services-component" >
    <services-list v-for="service in services"
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

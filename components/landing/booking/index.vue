<template>
  <div class="booking-component">
    <v-tabs-items v-model="page" class="booking-container">
      <v-tab-item
        v-for="(p, index) in pages"
        :key="p"
      >
        <div v-if="page == 0" flat class="booking-page-1">
          <booking-card v-for="(booking, index) in bookings"
                        :key="index"
                        :booking="booking"
                        @switch="switchBooking"

          />
        </div>
        <div v-if="page == 1" flat class="booking-page-2">
          <booking-app @switch="switchBooking" />
        </div>
      </v-tab-item>
    </v-tabs-items>
  </div>
</template>

<script>
  import bookingCard from './booking-card'
  import bookingApp from './booking-app'

  export default {
    name: "index",
    props: {
      bookings: {
        type: Array,
        default: () => []
      }
    },
    components: {
      bookingCard, bookingApp
    },
    data () {
      return {
        pages: [1, 2],
        page: 0
      }
    },
    methods: {
      switchBooking () {
        return this.page == 1 ? this.page = 0 : this.page = 1
      }
    }
  }
</script>

<style scoped>

  .booking-component {
    max-width: 650px;
    margin: 0 auto;
    padding-bottom: 5rem;
  }

  .booking-page-1, .booking-page-2 {
    height: 725px;;
    width: 100%;
    padding: 0 1rem;
  }

  .booking-container {
    max-width: 1024px;
    margin: 0 auto;
  }
</style>

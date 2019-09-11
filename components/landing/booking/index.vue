<template>
  <div class="booking-component">
    <v-tabs-items v-model="page" class="booking-container">
      <v-tab-item
        v-for="(p, index) in pages"
        :key="p"
      >
        <div v-if="page == 0" flat class="booking-page-1">
          <booking-card v-for="booking in bookings"
                        :booking="booking"

          />
        </div>
        <v-card v-if="page == 1" flat class="booking-page-2">
          <v-card-text>
            goodbye
          </v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </div>
</template>

<script>
  import bookingCard from './booking-card'

  export default {
    name: "index",
    props: {
      bookings: {
        type: Array,
        default: () => []
      }
    },
    components: {
      bookingCard
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
  }

  .booking-page-1, .booking-page-2 {
    height: 200px;
    width: 100%;
    padding: 0 1rem;
  }

  .booking-container {
    max-width: 1024px;
    margin: 0 auto;
  }
</style>

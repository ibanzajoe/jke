<template>
  <div class="booking-card">
    <h1 class="booking-card-title">
      {{booking.type}}
    </h1>
    <div class="booking-card-content-container">
      <div class="content-label">
        <h2 class="content-label-title">
          {{booking.type}}
        </h2>
        <h3 class="content-label-description">
          {{booking.description}}
        </h3>
      </div>
      <div class="content-action">
        <h3 class="content-label-description">
          {{booking.time}} | {{booking.price}}
        </h3>
        <v-btn @click="$emit('switch')" outlined class="book-button" large >BOOK</v-btn>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "booking-card",
    props: {
      booking: {
        type: Object,
        default: () => {}
      }
    }
  }
</script>

<style scoped>

  .booking-card {
    border-bottom: 1px solid rgb(226, 226, 226);
    padding-top: 40px;
  }
  .booking-card:last-child {
    border-bottom: 0;
  }
  .booking-card-content-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .booking-card-title {
    font-size: 30px;
    margin-bottom: 30px;
    color: rgb(95, 11, 53);
  }

  .content-label-description {
    margin-top: 5px;
    font-size: 16px;
    line-height: 1.5;
    color: rgb(94,94,94);
    font-weight: 400;
  }

  .booking-card-content-container {
    padding-bottom: 40px;
  }
  .content-label-title {
    font-size: 22px;
    line-height: 1.25;
    color: rgb(27,27,27);
  }

  .content-action {
    text-align: right;
  }

  .content-label-description {
    margin-bottom: 10px;
  }

  .book-button {
    border-color: rgb(95, 11, 53);
    color: rgb(95, 11, 53);
    border-radius: 0;
  }

  @media screen and (max-width: 600px) {
    .booking-card {
      padding-left: 2rem;
      padding-right: 2rem;
    }
    .booking-card-content-container {
      display: block;
    }
    .content-action {
      text-align: left;
    }
  }
</style>

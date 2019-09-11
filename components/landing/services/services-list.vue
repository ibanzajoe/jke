<template>
  <div class="services-list">
    <div class="services-type">
      <h3 class="type-heading">
        {{service.type}}
      </h3>
      <p class="type-subheading">
        {{service.description}}
      </p>
    </div>
    <v-layout class="service-listing" wrap>

      <v-flex  class="service-item"
               v-for="(item, index) in service.items"
               :key="index"
      >
        <div class="service-item-box">
          <div class="item-image-box">
            <img :src="item.image" alt="image" />
          </div>
          <div class="item-label-box">
            <div class="item-label">
              {{item.label}}
            </div>
            <div class="item-label-price">
              {{item.price}}
            </div>
          </div>
        </div>
      </v-flex>
    </v-layout>
    <hr class="service-end-border" />

  </div>
</template>

<script>
  export default {
    name: "services-list",
    props: {
      service: {
        type: Object,
        default: () => {}
      }
    }
  }
</script>

<style scoped>

  .type-heading, .type-subheading {
    text-align: center;
  }

  .type-heading {
    font-size: 22px;
    line-height: 1.25;
    text-indent: 1px;
    lettering-spacing: 1px;
  }

  .type-subheading {
    margin-top: 5px;
    font-size: 16px;
    color: rgb(89,89,89);
    font-style: italic;
    line-height: 1.5;
    font-weight: 400;
    overflow-wrap: break-word;
    word-wrap: break-word;
  }

  .services-type {
    margin-top: 40px;
  }

  .service-listing {
    margin-top: 40px;
    padding-top: 40px;
    padding-left: 2rem;
    padding-right: 2rem;
  }
  .service-item {
    padding: 0 20px;
    padding-bottom: 40px;
    max-width: 33.3333%;
    flex-basis: 33.3333%;
    font-size: 19px;
  }

  img {
    width: 100%;
  }

  .item-label-box {
    display: flex;
    align-items: start;
    margin-top: 30px;
  }

  .item-label {
    font-size: 16px;
    flex-basis: 100%;
    line-height: 1.25;
    text-indent: 2px;
    letter-spacing: 2px;
    text-transform: uppercase;
    font-weight: 700;
    color: rgb(27,27,27);
  }

  .item-label-price {
    flex-basis: 100px;
    text-align: right;
  }

  .service-end-border {
    font-size: 19px;
    margin-top: 10px;
    border-color: rgb(226, 226, 226);
    margin-bottom: 40px;
    border-style: solid;
    border-width: 0;
    border-bottom-width: 1px;
    width: 100%;
  }

  @media screen and (max-width: 1024px) {
    .service-item {
      padding: 0 20px;
      padding-bottom: 40px;
      max-width: 50%;
      flex-basis: 50%;
      font-size: 19px;
    }
  }

  @media screen and (max-width: 767px) {
    .service-item {
      max-width: 100%;
      flex-basis: 100%;
      padding-left: 50px;
      padding-right: 50px;
    }
  }
</style>

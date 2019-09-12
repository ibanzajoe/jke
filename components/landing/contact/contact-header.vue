<template>
  <v-layout class="contact-header" wrap flex-column>
    <h1 class="contact-title">
      {{text.heading}}
    </h1>
    <h2 class="contact-subheading">
      {{text.subheading}}
    </h2>
    <v-layout class="email-subscribe" align-center justify-center>
      <v-text-field v-model="email" placeholder="Email Address" class="email-form" />
      <v-btn outlined class="email-button">Subscribe</v-btn>
    </v-layout>

  </v-layout>
</template>

<script>
  export default {
    name: "contact-header",
    props: {
      text: {
        type: Object,
        default: () => {}
      }
    },
    data () {
      return {
        email: null
      }
    }
  }
</script>

<style scoped>

  .contact-title {
    font-size: 36px;
    margin-bottom: 15px;
    line-height: 1.25;
    text-indent: 1px;
    letter-spacing: 1px;
    text-align: center;
    color: rgb(27, 27, 27);
  }

  .contact-subheading {
    font-size: 16px;
    margin-bottom: 15px;
    line-height: 1.5;
    color: rgb(94, 94, 94);
    font-weight: 400;
    overflow-wrap: break-word;
    margin-top: 15px;
    text-align: center;
  }

  .email-subscribe {
    width: 100%;
    max-width: 66.66%;
    margin: 0 auto;
  }

  .email-form /deep/ input {
    padding-left: 1rem;
  }

  .email-button {
    text-transform: uppercase;
    border-color: rgb(95, 11, 53);
    margin-left: 1rem;
    color: rgb(95, 11, 53);
    border-radius: 0;
  }
</style>

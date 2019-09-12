<template>
  <v-layout>
    <v-flex xs6>
      <contact-block :content="content" />
    </v-flex>
    <v-flex class="contact-map" xs6>
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3305.0828711711756!2d-118.4075297484083!3d34.06738982428242!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80c2bbf7f01c2727%3A0x108a11769efcde94!2s9666%20Brighton%20Way%2C%20Beverly%20Hills%2C%20CA%2090210!5e0!3m2!1sen!2sus!4v1568297360996!5m2!1sen!2sus"
              width="100%" height="100%" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
    </v-flex>
  </v-layout>
</template>

<script>
  import contactBlock from './contact-block'

  export default {
    name: "contact-content",
    props: {
      content: {
        type: Array,
        default: () => []
      },
      map: {

      }
    },
    components: {
      contactBlock
    }
  }
</script>

<style scoped>

  .contact-map iframe {
    height: 100%;
  }
</style>

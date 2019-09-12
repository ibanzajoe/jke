<template>
  <div class="contact-index">
    <contact-header :text="contact.headers" />

    <contact-content :content="contact.content" :map="contact.map" />

  </div>
</template>

<script>
  import contactHeader from './contact-header'
  import contactContent from './contact-content'

  export default {
    name: "index",
    props: {
      contact: {

      }
    },
    components: {
      contactHeader, contactContent
    }
  }
</script>

<style scoped>

  .contact-index {
    height: 200px;
    width: 100%;
  }
</style>

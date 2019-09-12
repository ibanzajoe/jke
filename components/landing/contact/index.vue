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
    width: 100%;
    padding-bottom: 40px;
    padding-left: 20px;
    padding-right: 20px;
  }
</style>

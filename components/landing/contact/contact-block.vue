<template>
  <div class="content-block">
    <div class="content-section"
         v-for="(data, index) in content"
         :key="index"
    >
      <h1 class="content-section-heading">
        {{data.heading}}
      </h1>
      <h2 v-if="data.content != 'time'" class="content-section-content">
        {{data.content}}
      </h2>
      <div v-if="data.content == 'time'">
        <h2 v-for="t in data.time" class="content-section-content">
          {{t}}
        </h2>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    name: "contact-block",
    props: {
      content: {
        type: Object,
        default: () => {}
      }
    }
  }
</script>

<style scoped>

  .content-block {
    max-width: 70%;
    margin: 0 auto;
    padding: 70px 20px;
  }

  .content-section {
    padding-left: 20px;
    padding-right: 20px;
    padding-bottom: 40px;
  }

  .content-section-heading {
    font-size: 16px;
    flex-basis: 100%;
    line-height: 1.25;
    text-indent: 2px;
    letter-spacing: 2px;
    text-transform: uppercase;
    font-weight: 700;
    color: rgb(27,27,27);
    margin-bottom: 20px;
  }

  .content-section-content {
    font-size: 16px;
    line-height: 1.5;
    color: rgb(94, 94, 94);
    font-weight: 400;
    overflow-wrap: break-word;
  }
</style>

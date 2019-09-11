<template>
  <div class="divider">
    <hr class="hr" />
  </div>
</template>

<script>
  export default {
    name: "divider"
  }
</script>

<style scoped>

  .divider {
    font-size: 19px;
    opacity: 0.01;
    background-color: rgb(95, 11, 53);
  }

  .hr {
    border-width: 3px;
    margin-bottom: 50px;
    border-color: rgb(246, 82, 155);
    opacity: 0.01s;
    border-style: solid;
    background-color: rgb(95, 11, 53);
    font-size: 19px;
    width: 100%;
    height: 0;
  }
</style>

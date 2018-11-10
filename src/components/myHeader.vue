<template>
  <div class='my-header-container'>
    <title>
      Весь мир TRAVEL
    </title>
  </div>
</template>

<script>
  export default {
    name: 'myHeader',
  };
</script>

<style scoped>
  title {
    font-size: 32px;
    margin: 20px 30px;
    display: block;
  }
  .my-header-container {
    margin-left: 200px;
    overflow: hidden;
    max-height: 200px;
    min-height: 20px;
    background: #64A8D1;
    height: initial;
  }
</style>

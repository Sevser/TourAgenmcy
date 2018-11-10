<template>
  <div class='myHeader'>
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
    font-family: 'Comic Sans MS';
    font-size: 16px;
    margin: 20px 30px;
    display: block;
  }
  .myHeader {
    position: absolute;
    left: 200px;
    right: 0;
    top: 0;
    max-height: 200px;
    min-height: 20px;
    background: #64A8D1;
    height: initial;
  }
</style>

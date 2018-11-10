<template>
  <div class="logo">
    <img src="./../assets/logo.jpg" alt="Логотип">
  </div>
</template>

<script>
  export default {
    name: 'Logo',
  };
</script>

<style scoped>
  .logo {
    position: absolute;
    top: 0;
    left: 0;
    width: 200px;
    height: 200px;
  }
  img {
    width: 100%;
    height: 100%;
  }
</style>

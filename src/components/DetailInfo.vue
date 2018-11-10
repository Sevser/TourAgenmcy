<template>
  <div class="detail-info-container">
    <div class="title">
      {{data[current].title}}
    </div>

  </div>
</template>

<script>
  export default {
    name: 'DetailInfo',
    props: {
      current: String,
      data: Array,
    },
  };
</script>

<style scoped>
  .detail-info-container {
    width: 55%;
    height: 100%;
    background: white;
    opacity: 0.97;
    margin: auto;
    padding: 20px;
  }
  .title {
    font-size: 40px;
  }
</style>

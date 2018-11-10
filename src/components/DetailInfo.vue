<template>
  <div class="detail-info-container">
    <div class="title">
      {{data[current].title}}
    </div>
    <mapBody v-if="data[current].name === 'contacts'">
    </mapBody>
  </div>
</template>

<script>
  import mapBody from './mapBody';

  export default {
    name: 'DetailInfo',
    components: {
      mapBody,
    },
    props: {
      current: Number,
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
    position: relative;
  }
  .title {
    font-size: 40px;
  }
</style>

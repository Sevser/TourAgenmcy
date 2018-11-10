<template>
  <div class="body" v-bind:style="getBackground">

  </div>
</template>

<script>
  export default {
    name: 'background',
    props: {
      index: Number,
      imageSrc: Array,
    },
    computed: {
      getBackground() {
        return `background: url( ${this.imageSrc[this.index].image}) center no-repeat / 100% 100%;`;
      },
    },
  };
</script>

<style scoped>
  .body {
    height: 100%;
    width: 100%;
    -moz-background-size: 100%; /* Firefox 3.6+ */
    -webkit-background-size: 100%; /* Safari 3.1+ и Chrome 4.0+ */
    -o-background-size: 100%; /* Opera 9.6+ */
    background-size: 100%; /* Современные браузеры */
    -webkit-transition-duration: 2s;
    -o-transition-duration: 2s;
    -moz-transition-duration: 2s;
    transition-duration: 2s;
    position: fixed;
  }
</style>

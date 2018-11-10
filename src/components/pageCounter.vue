<template>
  <div class="page-counter-container">
    <div v-for="index in length">
      <div class="item"
           :class="{ 'active' : index === current }"
            @click="change(index)"></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'pageCounter',
    props: {
      length: Number,
      current: Number,
    },
    methods: {
      change(index) {
        this.$emit('changePage', index - 1);
      },
    },
  };
</script>

<style scoped>
  .page-counter-container {
    position: absolute;
    right: 20px;
    top: 45%;
    z-index: 1;
  }
  .item {
    height: 16px;
    width: 16px;
    border-radius: 20px;
    margin: 5px;
    border-width: 3px;
    border-color: white;
    border-style: solid;
    background: transparent;
  }
  .active {
    background: whitesmoke;
  }
</style>

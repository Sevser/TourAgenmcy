<template>
  <main>
    <myHeader></myHeader>

  </main>

</template>

<script>
  import myHeader from './myHeader';

  export default {
    name: 'Body',
    components: {
      myHeader,
    },
  };
</script>

<style scoped>
  main {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
  }
</style>

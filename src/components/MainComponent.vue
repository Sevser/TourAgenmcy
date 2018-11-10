<template>
  <div class="MainComponent">
    <dataContainer></dataContainer>
    <logo></logo>
  </div>
</template>

<script>
  import dataContainer from './Body';
  import logo from './Logo';

  export default {
    name: 'MainComponent',
    components: {
      dataContainer,
      logo,
    },
    data() {
      return {
        msg: '',
      };
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>

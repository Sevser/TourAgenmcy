<template>
    <div id="map">

    </div>
</template>

<script>
  import ymaps from 'ymaps';

  export default {
    name: 'mapBody',
    data() {
      return {
        myMap: {},
      };
    },
    mounted() {
      ymaps.load().then((maps) => {
        this.myMap = new maps.Map('map', {
          center: [55.876521, 37.507850],
          zoom: 15,
        });
      });
    },
  };
</script>

<style scoped>
 #map {
   height: 80%;
   width: 60%;
 }
</style>

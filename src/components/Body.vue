<template>
  <main v-on:scroll.passive="handleScroll">
    <div class='myHeader'>
      <myHeader></myHeader>
    </div>
    <div style="z-index: 0">
      <Background
        :index="index"
        :imageSrc="pageData"></Background>
    </div>
    <div class="detail-info-block">
      <DetailInfo
        :data="pageData"
        :current="index"></DetailInfo>
    </div>
    <pageCounter
      :length="pageData.length"
      :current="index+1"
      @changePage="setPage($event)"></pageCounter>
  </main>

</template>

<script>
  import myHeader from './myHeader';
  import Background from './background';
  import DetailInfo from './DetailInfo';
  import pageCounter from './pageCounter';

  export default {
    name: 'Body',
    components: {
      myHeader,
      Background,
      DetailInfo,
      pageCounter,
    },
    data() {
      return {
        index: 0,
        pageData: [
          {
            name: 'seaHoliday',
            image: '/static/img/Kaputas-Beach.jpg',
            title: 'Отдых на Море',
          },
          {
            name: 'activeHoliday',
            image: '/static/img/winter.jpg',
            title: 'Активный отдых',
          },
          {
            name: 'europe',
            image: 'http://driving24.ru/wp-content/uploads/2014/10/4336.jpg',
            title: 'Путешествия по Европе',
          },
          {
            name: 'bashkiriya',
            image: 'http://konkurs.trip2rus.ru/sites/default/files/field/images/foto/p8022054.jpg',
            title: 'Отдых в Башкирии',
          },
          {
            name: 'contacts',
            image: '/static/img/AboutUs.jpg',
            title: 'Наши контакты',
          },
          {
            name: 'socialNetwork',
            image: '/static/img/socialNetwork.jpg',
            title: 'Наши Социальные сети',
          },
        ],
        canScroll: true,
      };
    },
    methods: {
      handleScroll(event) {
        if (!this.canScroll) {
          return;
        }
        if (event.deltaY > 0) {
          if (this.index < (this.pageData.length - 1)) {
            this.index = this.index + 1;
          }
        } else if (this.index > 0) {
          this.index = this.index - 1;
        }
        this.canScroll = false;
        setTimeout(() => { this.canScroll = true; }, 2000);
      },
      setPage(index) {
        this.index = index;
      },
    },
    created() {
      window.addEventListener('wheel', this.handleScroll);
    },
    destroyed() {
      window.removeEventListener('wheel', this.handleScroll);
    },
  };
</script>

<style scoped>
  main {
    position: absolute;
    overflow-y: hidden;
    height: 100%;
    width: 100%;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
  }
  .myHeader {
    height: initial;
    position: relative;
    top: 0;
    left: 0;
    right: 0;
  }
  .detail-info-block {
    height: 100%;
  }
</style>

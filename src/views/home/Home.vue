<template>
  <div>
    <home-header></home-header>
    <home-swiper :swiperList='swiperList'></home-swiper>
    <home-icons :iconList="iconList"></home-icons>
    <home-recommend :recommendList="recommendList"></home-recommend>
    <home-weekend :weekendList="weekendList"></home-weekend>
  </div>
</template>

<script>
  import HomeHeader from './components/Header'
  import HomeSwiper from './components/Swiper'
  import HomeIcons from './components/Icons'
  import HomeRecommend from './components/Recommend'
  import HomeWeekend from './components/Weekend'
  import axios from 'axios';
  import { mapState } from 'vuex';
  export default {
    name: "home",
    components: {
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeRecommend,
      HomeWeekend
    },
    data() {
      return {
        lastCity:'',
        swiperList: [],
        iconList: [],
        recommendList: [],
        weekendList: []
      }
    },
    methods: {
      async getHomeInfo() {
        const index = await axios.get('/static/mock/index.json?/' + this.city);
        const res = index.data;
        if (res.ret && res.data) {
          this.swiperList = res.data.swiperList;
          this.iconList = res.data.iconList;
          this.recommendList = res.data.recommendList;
          this.weekendList = res.data.weekendList;
        }
      }
    },
    mounted() {
      this.lastCity=this.city;
      this.getHomeInfo()
    },
    computed: {
      ...mapState(['city'])
    },
    activated(){
    if(this.lastCity!==this.city){
      this.lastCity=this.city;
      this.getHomeInfo()
    }
    }
  };
</script>
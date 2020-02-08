<template>
<div class="header">
  <div class="header-left ">
   <span class="iconfont back-icon">&#xe618;</span>
  </div>
  <div class="header-input">
    <span class="iconfont">&#xe61d;</span>
   输入城市/景点，游玩/主题
  </div>
  <router-link to='/city'>
    <div class="header-right">
      <span class="iconfont arrow-icon">&#xe64a;</span>
     {{this.city}}
    </div>
  </router-link>
</div>
</template>

<script>
  import {mapState} from 'vuex';
export default {
  name: "HomeHeader",
  computed:{
    ...mapState(['city'])
  }
};
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import './header.styl';
</style>
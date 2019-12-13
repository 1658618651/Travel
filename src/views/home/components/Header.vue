<template>
<div class="header">
  <div class="header-left ">
   <span class="iconfont back-icon">&#xe624;</span>
  </div>
  <div class="header-input">
    <span class="iconfont">&#xe632;</span>
   输入城市/景点，游玩/主题
  </div>
  <div class="header-right">
    <span class="iconfont arrow-icon">&#xe64a;</span>
   {{this.city}}
  </div>
</div>
</template>

<script>
export default {
  name: "HomeHeader",
  props: {
    city: String
  }
};
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import './header.styl';
</style>
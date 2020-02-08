<template>
    <div class="header">
        城市选择
        <router-link to='/'> <span class="iconfont header-back">&#xe618;</span></router-link>
    </div>
</template>

<script>

</script>

<style lang=stylus scoped>
    @import '~styles/varibles.styl';

    .header {
        position: relative;
        overflow: hidden;
        height: .86rem;
        line-height: .86rem;
        text-align: center;
        color: #fff;
        font-size: .32rem;
        background: $bgColor;
    }

    .header-back {
        width: .64rem;
        font-size: .32rem;
        text-align: center;
        position: absolute;
        top: 0;
        left: 0;
        color: #fff;
    }
</style>
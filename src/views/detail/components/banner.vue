<template>
    <div class="banner">
        <img class='banner-img'
            src="//img1.qunarzz.com/sight/p0/201403/03/95666b4b57b3ef508a9cd52ffda638a0.jpg_600x330_92ba5280.jpg" />
        <div class="banner-info">
            <div class="banner-title">八达岭长城(AAAAA景区)</div>
            <div class="banner-number"><span class="iconfont banner-icon">&#xe64b;39</span></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'DetailBanner',

    }
</script>
<style lang='stylus' scoped>
    @import '~styles/varibles.styl';
    @import '~styles/mixins.styl';

    .banner {
        position: relative;
        overflow: hidden;
        height: 0;
        padding-bottom: 55%;
    }

    .banner-img {
        width: 100%;
    }
    .banner-info{
        display: flex;
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0;
        line-height: .6rem;
        color: #ccc;
        background-image: linear-gradient(top, rgba(0,0,0,0),rgba(0,0,0,0.8));
    }
    .banner-title{
        flex: 1;
        font-size: .32rem;
        padding: 0 .2rem;
    }
    .banner-number{
        margin-top: .14rem;
        padding: 0 .4rem;
        line-height: .32rem;
        height: .32rem;
        border-radius: .2rem;
        background: reba(0,0,0,0.8);
        font-size: .24rem;
    }
    .banner-icon{
        font-size: .24rem;
    }
</style>
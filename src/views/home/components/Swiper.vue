<template>
    <swiper :options="swiperOption" class="swiper" v-if="show">
        <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src='item.imgUrl' />
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
</template>
<script>
    export default {
        name: 'HomeSwiper',
        props:{
            swiperList:Array
        },
        data() {
            return {
                swiperOption: {
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true,       
                    },
                    loop:true,
                },
            }
        },
        computed: {
            show(){
                return this.swiperList.length;
            }
        },
    }
</script>
<style lang="stylus" scoped>
    * {
        touch-action: none;
    }

    .swiper>>>.swiper-pagination-bullet-active {
        /* swiper下面的所有swiper-pagination-bullet-active都变化 */
        background: #fff !important;
    }

    .swiper {
        overflow: hidden;
        width: 100%;
        height: 0;
        padding-bottom: 26.67%;
        /* 即高始终为宽的31.25% */
    }

    .swiper-img {
        width: 100%
    }
</style>
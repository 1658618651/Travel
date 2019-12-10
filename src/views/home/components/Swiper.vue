<template>
    <swiper :options="swiperOption" class="swiper">
        <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src='item.imgUrl' />
        </swiper-slide>
        <!-- <swiper-slide>
            <img class="swiper-img"
                src='http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/f74957827d190508c2598fb79ec36102.jpg_750x200_2960f17f.jpg' />
        </swiper-slide>
        <swiper-slide>
            <img class="swiper-img"
                src='http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9accc56ec000de669ce90d0b3f44af86.jpg_750x200_b35b86a0.jpg' />
        </swiper-slide>
        <swiper-slide>
            <img class="swiper-img"
                src='http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/f74957827d190508c2598fb79ec36102.jpg_750x200_2960f17f.jpg' />
        </swiper-slide>
        <swiper-slide>
            <img class="swiper-img"
                src='http://img1.qunarzz.com/piao/fusion/1812/48/5713e2a2ba72f902.jpg_750x200_2b382dac.jpg' />
        </swiper-slide>
        <swiper-slide>
            <img class="swiper-img"
                src='http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9b917df77076d8aea3defd6944c82d74.jpg_750x200_9f7827d2.jpg' />
        </swiper-slide>
        <swiper-slide>
            <img class="swiper-img"
                src='http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9accc56ec000de669ce90d0b3f44af86.jpg_750x200_b35b86a0.jpg' />
        </swiper-slide> -->
        <!-- Optional controls -->
        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
</template>
<script>
    export default {
        name: 'HomeSwiper',
        data() {
            return {
                swiperOption: {
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true,       
                    },
                    loop:true,
                },
                swiperList: [{
                        id: '0001',
                        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/1d8faa9f4d49b77ca1e61e2b478260f7.jpg_750x200_25cf76e2.jpg'
                    },
                    {
                        id: '0002',
                        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/f74957827d190508c2598fb79ec36102.jpg_750x200_2960f17f.jpg'
                    },{
                        id: '0003',
                        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9accc56ec000de669ce90d0b3f44af86.jpg_750x200_b35b86a0.jpg'
                    },
                    {
                        id: '0004',
                        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1812/48/5713e2a2ba72f902.jpg_750x200_2b382dac.jpg'
                    },{
                        id: '0005',
                        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9b917df77076d8aea3defd6944c82d74.jpg_750x200_9f7827d2.jpg'
                    },
                    {
                        id: '0006',
                        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9accc56ec000de669ce90d0b3f44af86.jpg_750x200_b35b86a0.jpg'
                    },{
                        id: '0007',
                        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9accc56ec000de669ce90d0b3f44af86.jpg_750x200_b35b86a0.jpg'
                    }
                    ]
            }
        }
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
<template>
    <swiper :options="swiperOption" class="swiper">
        <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icons">
            <div class="icon" v-for="item of page" :key="item.id">
                <div class="icon-img">
                    <img :src="item.imgUrl" class="icon-img-content" />
                </div>
                <p class="icon-desc">{{item.desc}}</p>
            </div>
        </div>
        </swiper-slide>
        <!-- <swiper-slide>
        <div class="icons">
            <div class="icon" v-for="item of iconList" :key="item.id">
                <div class="icon-img">
                    <img :src="item.imgUrl" class="icon-img-content" />
                </div>
                <p class="icon-desc">{{item.desc}}</p>
            </div>
        </div>
        </swiper-slide> -->
        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
</template>

<script>
    export default {
        name: 'HomeIcons',
        data() {
            return {
                swiperOption: {
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true,       
                    },
                    loop:true,
                },
                iconList: [{
                    id: '0001',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                    desc: '景点门票'
                },
                {
                    id: '0002',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
                    desc: '故宫'
                }, {
                    id: '0003',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                    desc: '北京必游'
                },
                {
                    id: '0004',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
                    desc: '南宫养生温泉'
                }, {
                    id: '0005',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                    desc: '一日游'
                },
                {
                    id: '0006',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
                    desc: '古北水镇'
                }, {
                    id: '0007',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fc/b10a6b2e4f0fe102.png',
                    desc: '北京滑雪'
                }, {
                    id: '0008',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/c1/6f15f887179fa002.png',
                    desc: '颐和园'
                },
                {
                    id: '0009',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
                    desc: '故宫'
                }
                ]
            }
        },
    computed: {
        pages(){
            const pages=[];
            this.iconList.forEach((item,index)=>{
                const page=Math.floor(index/8);
                if(!pages[page]){
                    pages[page]=[];
                }
                pages[page].push(item);
            })
            return pages;
        }
    },
    }
</script>
<style lang='stylus' scoped>
    @import '~styles/varibles.styl';
    @import '~styles/mixins.styl';
    .icons >>>.swiper-container {
        overflow: hidden;
        height: 0;
        padding-bottom: 50%;
        /* 即高始终为宽的50% */
    }
    .icons{
        margin-top: .1rem;
    }
    .icon {
        position: relative;
        overflow: hidden;
        float: left;
        width: 25%;
        height: 0;
        padding-bottom: 25%;
        /* 即高始终为宽的25% */
    }

    .icon-img {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: .44rem;
        box-sizing: border-box;
        padding: .1rem;
    }

    .icon-img-content {
        display: block;
        margin: 0 auto;
        height: 100%;
    }

    .icon-desc {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        line-height: .44rem;
        height: .44rem;
        text-align: center;
        ellipsis();
        color: $darkTextColor;

    }
</style>
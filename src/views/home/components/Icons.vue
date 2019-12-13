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
        props:{
            iconList:Array
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
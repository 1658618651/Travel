<template>
        <div>
           <div class="recommend-title">周末去哪儿</div>
           <ul>
               <li class="item border-bottom" v-for="item of recommendList" :key='item.id'>
                   <div class='item-wrap'>
                        <img :src='item.imgUrl' class="item-img"/>
                   </div>
                   <div class="item-info">
                       <p class="item-title">{{item.title}}</p>
                       <p class="item-title">{{item.desc}}</p>
                   </div>
               </li>
           </ul>
        </div>
    
    </template>
    
    <script>
        export default {
            name:'HomeWeekend',
            data() {
                return {
                    recommendList: [{
                        id: '0001',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '故宫',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    },
                    {
                        id: '0002',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '圆明园',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    }, {
                        id: '0003',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '八达岭长城',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    },
                    {
                        id: '0004',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '颐和园',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    }, {
                        id: '0005',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '怀北国际滑雪场',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    },
                    {
                        id: '0006',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '南山滑雪场',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    }, {
                        id: '0007',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '天坛公园',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    }, {
                        id: '0008',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '古北水镇',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    },
                    {
                        id: '0009',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '鸟巢',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    },
                    {
                        id: '0010',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                        title: '什刹海',
                        desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                    }
                    ]
                }
            }
        }
    </script>
    
    <style lang="stylus" scoped>
    @import '~styles/mixins.styl';
    .recommend-title{
        line-height: .8rem;
        background: #eee;
        text-indent: .2rem;
        margin-top: .2rem;
    }
    .item-wrap{
        height: 0;
        overflow: hidden;
        padding-bottom: 33.9%;
    }
    .item-img{
        width: 100%;
    }
    .item-info{
        padding: .1rem;
    }
    .item-title{
        line-height: .54rem;
        font-size: .32rem;
        ellipsis();
    }
    .item-title{
        line-height: .4rem;
        color: #ccc;
        ellipsis()
    }
    </style>
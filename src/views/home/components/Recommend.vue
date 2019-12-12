<template>
    <div>
       <div class="recommend-title">热销推荐</div>
       <ul>
           <li class="item border-bottom" v-for="item of recommendList" :key='item.id'>
                   <img :src='item.imgUrl' class="item-img"/>
               <div class="item-info">
                   <p class="item-title">{{item.title}}</p>
                   <p class="item-title">{{item.desc}}</p>
                   <button class="item-button">查看详情</button>
               </div>
           </li>
       </ul>
    </div>

</template>

<script>
    export default {
        name:'HomeRecommend',
        data() {
            return {
                recommendList: [{
                    id: '0001',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
                    title: '故宫',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                },
                {
                    id: '0002',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/f5/f5f45e1a83537bcb.water.jpg_250x250_63e3520a.jpg',
                    title: '圆明园',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                }, {
                    id: '0003',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_250x250_50c99cf3.jpg',
                    title: '八达岭长城',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                },
                {
                    id: '0004',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/d2/d274c92de14c93da.water.jpg_250x250_d852635b.jpg',
                    title: '颐和园',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                }, {
                    id: '0005',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1711/c2/c2f78ad1e34fe4dea3.img.jpg_250x250_6e1f98c0.jpg',
                    title: '怀北国际滑雪场',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                },
                {
                    id: '0006',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1511/d2/d2aec2dfc5aa771290.water.jpg_250x250_7b67daa3.jpg',
                    title: '南山滑雪场',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                }, {
                    id: '0007',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/92/920e47352552c1c990.water.jpg_250x250_ee99c18e.jpg',
                    title: '天坛公园',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                }, {
                    id: '0008',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1903/5d/5dcaf453dfd6f5dba3.img.jpg_250x250_ad9c739f.jpg',
                    title: '古北水镇',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                },
                {
                    id: '0009',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/fe/434ee530e21f1c11bad088e8cc8d5e93.water.jpg_250x250_12e8154c.jpg',
                    title: '鸟巢',
                    desc:'查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情查看详情'
                },
                {
                    id: '0010',
                    imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/85/85c883189bf7293390.water.jpg_250x250_090a42b6.jpg',
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
.item{
    display: flex;
    overflow: hidden;
    height: 1.9rem;
}
.item-img{
    width: 1.7rem;
    height: 1.7rem;
    padding: .1rem;
}
.item-info{
    flex: 1;
    padding: .1rem;
    min-width: 0;
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
.item-button{
    background: #ff9300;
    padding: 0 .2rem;
    border-radius: .06rem;
    color: #fff;
    line-height: .4rem;
    margin-top: .16rem;

}
</style>
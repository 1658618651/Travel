<template>
        <div>
           <div class="recommend-title">周末去哪儿</div>
           <ul>
               <li class="item border-bottom" v-for="item of weekendList" :key='item.id'>
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
            props:{
                weekendList:Array
            }
                }
            
        
    </script>
    
    <style lang="stylus" scoped>
    @import '~styles/mixins.styl';
    .recommend-title{
        line-height: .8rem;
        background: #eee;
        text-indent: .2rem;
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
<template>
  <div class="hot">
    <div class="title">
      <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="">
      <span class="mp-title">本周热门榜单</span>
      <a class="right-title" href="#">全部榜单<i class="iconfont icon-iconfontjiantou2"></i></a>
    </div>
    <ul class="mp-hotsale-list" >
      <li class="mp-hotsale-item" v-for="(item,index) in hotList" :key="item.id">
        <a href="#">
          <div class="top" v-if="item.top"><img :src='item.top'></div>
          <div class="top-img"><img :src="item.imgUrl" alt=""></div>
          <div class="mp-hotsale-sight">{{item.desc}}</div>
          <div class="mp-hotsale-price">
            <span class="mpg-price">￥<em class="mpg-price-num">{{item.price}}</em>
            </span>起
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
    export default {
        name: "hot",
        data() {
            return {
              hotList:[
                {
                  id:'0001',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
                  desc:'故宫',
                  price:60,
                  top:'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png'
                },
                {
                  id:'0002',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_250x250_50c99cf3.jpg',
                  desc:'八达岭长城',
                  price:40,
                  top:'http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png'
                },
                {
                  id:'0003',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_250x250_3588bc9a.jpg',
                  desc:'北京世界园',
                  price:108,
                  top:'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png'
                },
                {
                  id:'0004',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1505/d2/d274c92de14c93da.water.jpg_250x250_d852635b.jpg',
                  desc:'颐和园',
                  price:30,
                },
                {
                  id:'0005',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/201403/24/92759d9d52af059a7849f482f10358c5.jpg_250x250_bb4897b4.jpg',
                  desc:'平谷桃花海',
                  price:31.9,
                },
                {
                  id:'0006',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_250x250_6c4c9885.jpg',
                  desc:'北京欢乐谷',
                  price:195,
                },
                {
                  id:'0007',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1705/7b/7bc3480c17245bd3a3.img.jpg_250x250_397be0d7.jpg',
                  desc:'淮北高山漂流',
                  price:118,
                },
                {
                  id:'0008',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_250x250_b8d94d62.jpg',
                  desc:'北京野生动物园',
                  price:119,
                },
                {
                  id:'0009',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1508/c0/0ddded36771ed10c9e03eb64794610cb.water.jpg_250x250_02467a25.jpg',
                  desc:'仙栖洞',
                  price:44,
                },
                {
                  id:'0010',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_250x250_ecfa0df2.jpg',
                  desc:'水立方',
                  price:54,
                },
              ]
            }
        }
    }
</script>

<style scoped lang="stylus">
 .hot{
   background-color: #fff;
   margin-top:0.2rem;
   .title{
     position: relative;
     padding: .24rem 0 .26rem;

     .title-img{
       display: inline-block;
       overflow: hidden;
       width: .3rem;
       height: .3rem;
       margin-left: .2rem;
       vertical-align: top;
     }
     .mp-title{
       display: inline-block;
       margin-left: .08rem;
       height: .44rem;
       color: #212121;
       font-size: .32rem;
       line-height: .44rem;
     }
     .right-title{
       position: absolute;
       top: .36rem;
       right: .32rem;
       color: #616161;
       font-size: .24rem;
       line-height: .28rem;
     }
     }
   .mp-hotsale-list{
     padding: 0 .24rem;
     overflow-x: scroll;
     white-space: nowrap;
     .mp-hotsale-item{
       position: relative;
       display: inline-block;
       padding: .06rem .06rem .2rem;
       width: 2rem;
       .top{
         position: absolute;
         top: 0;
         left: 0;
         z-index: 1;
         overflow: hidden;
         width: .84rem;
         height: .4rem;
         img{
           width: 0.84rem;
           height :0.4rem;
           vertical-align middle
         }
       }
       .top-img{
         overflow: hidden;
         width: 2rem;
         height: 0;
         padding-bottom: 100%;
         img{
           width 100%
         }
       }
       .mp-hotsale-sight{
         margin-top: .12rem;
         color: #212121;
         font-size: .28rem;
         line-height: .32rem;
         text-align: center;
       }
       .mp-hotsale-price{
         color: #616161;
         font-size: .28rem;
         line-height: .36rem;
         text-align: center;
         .mpg-price{
           color: #ff8300
         }
         .mpg-price-num{
           color: #ff8300
         }
       }
     }
   }

   }

</style>

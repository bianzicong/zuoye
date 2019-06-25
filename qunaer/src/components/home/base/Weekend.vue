<template>
   <div class="weekend-trip">
     <h2 class="mp-modtitle">周末去哪儿</h2>
     <div>
       <div class="mp-product-item" v-for="(item,index) in weekList" :key="item.id">
         <a href="#">
           <div class="product-imgcontainer">
             <img :src="item.imgUrl" alt="">
           </div>
           <div class="mp-product-info">
             <p class="product-name">{{item.name}}</p>
             <p class="product-desc">{{item.desc}}</p>
           </div>
         </a>
       </div>
     </div>
     <div class="mp-price-desc">
       <span class="iconfont icon-jinggao"></span>
       <div class="mp-price-desc-info">
         <span>票面价</span>是指通过景区指定窗口售卖的纸质门票上标注的价格
       </div>
     </div>
   </div>
</template>

<script>
    export default {
        name: "Weekend",
        data() {
            return {
              weekList:[
                {
                  id:'0001',
                  imgUrl:'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                  name:'京城周末撒欢',
                  desc:'在帝都过周末，不仅仅是城中游!'
                },
                {
                  id:'0002',
                  imgUrl:'http://img1.qunarzz.com/sight/source/1811/7e/476589267ebb41.jpg_r_640x214_bf599709.jpg',
                  name:'京城溜娃必去',
                  desc:'德智体美劳全面发展的亲子日，这些地方该去看看…!'
                },
                {
                  id:'0003',
                  imgUrl:'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
                  name:'帝都必打卡',
                  desc:'来北京必去的景点非这些地方莫属'
                },
                {
                  id:'0004',
                  imgUrl:'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
                  name:'寻找北京的皇城范儿',
                  desc:'数百年的宫廷庙宇，至今依旧威严霸气'
                },
                {
                  id:'0005',
                  imgUrl:'http://img1.qunarzz.com/sight/source/1505/ce/bc89bc2f0e33ea.jpg_r_640x214_3e408453.jpg',
                  name:'学生最爱的博物馆',
                  desc:'周末干嘛？北京很多博物馆已经免费开放啦'
                },
              ]
            }
        }
    }
</script>

<style scoped lang="stylus">
  .weekend-trip{
    .mp-modtitle{
      height: .8rem;
      padding-left: .26rem;
      line-height: .8rem;
      color: #212121;
      font-family: tahoma,arial,"Hiragino Sans GB","\5FAE\8F6F\96C5\9ED1",simsun,sans-serif;
    }
    .mp-product-item{
      position: relative;
      margin-bottom: .1rem;
      background: #fff;
    }
    .product-imgcontainer{
      overflow: hidden;
      height: 0;
      padding-bottom: 37.4375%;
      img{
        width :100%
      }
    }
    .mp-product-info{
      position: relative;
      padding: .14rem .2rem .2rem .2rem;
      .product-name{
        overflow: hidden;
        padding-right: 1.4rem;
        color: #212121;
        font-size: .28rem;
        line-height: .48rem;
        white-space: nowrap;
        text-overflow: ellipsis;
      }
      .product-desc{
        overflow: hidden;
        padding-right: 1.4rem;
        color: #616161;
        font-size: .24rem;
        line-height: .42rem;
        white-space: nowrap;
        text-overflow: ellipsis;
      }
    }
    .mp-price-desc{
      margin-top: .1rem;
      padding: .14rem .1rem;
      font-size: .24rem;
      line-height: .32rem;
      background: #fff;
      color: #616161;
      .iconfont{
        width: .24rem;
        display: block;
        float: left;
        line-height: .32rem;
      }
      .mp-price-desc-info{
        margin-left: .3rem;
        span{
          font-weight bold
        }
      }
    }
  }


</style>

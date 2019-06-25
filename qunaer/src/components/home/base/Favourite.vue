<template>
  <div class="favourite">
    <div class="mp-group-title">
      <img src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="">
      <span>猜你喜欢</span>
    </div>
    <ul class="mp-like-list">
      <router-link :to="{name:'Detail'}">
        <li class="mp-like-item mp-border-bottom" v-for="(item,index) in hotList" :key="item.id" >
          <a href="#" class="mp-fulllink">
            <div class="fulllink-img"><img :src="item.imgUrl" alt=""></div>
            <div class="mp-like-tag" :style="item.style">{{item.time}}</div>
            <div class="mp-like-info">
              <div class="mp-like-title mp-ellipsis">{{item.title}}</div>
              <div class="mp-like-comment">
                <i class="iconfont icon-icon-test"></i>
                <i class="iconfont icon-icon-test"></i>
                <i class="iconfont icon-icon-test"></i>
                <i class="iconfont icon-icon-test"></i>
                <i class="iconfont icon-icon-test"></i>
                <span>{{item.commentnum}}条评论</span>
              </div>
              <div class="mp-like-price">
                <span class="mpg-price">￥<em class="mpg-price-num">{{item.price}}</em></span>起
                <span class="mp-like-address">{{item.address}}</span>
              </div>
              <div class="mp-like-feature" v-if="item.desc">
                <div class="mp-ellipsis2">{{item.desc}}</div>
              </div>
            </div>
          </a>
        </li>
      </router-link>

    </ul>
    <a class="mp-like-more" href="#">查看所有产品</a>
  </div>
</template>

<script>
    export default {
        name: "favourite",
        data() {
            return {
              hotList:[
                {
                  id:'0001',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
                  style:'background-image:url(https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png)',
                  time:'可订明日',
                  title:'故宫',
                  commentnum:412707,
                  price:60,
                  address:'东城区',
                  desc:'世界五大宫之首，穿越与您近在咫尺'
                },
                {
                  id:'0002',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
                  style:'background-image:url(https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png)',
                  time:'随买随用',
                  title:'北京欢乐谷',
                  commentnum:70990,
                  price:195,
                  address:'朝阳区',
                  desc:'亚洲唯一飞行式过山车等你来挑战'
                },
                {
                  id:'0003',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
                  style:'background-image:url(https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png)',
                  time:'可订明日',
                  title:'故宫',
                  commentnum:32232,
                  price:60,
                  address:'东城区',

                },
                {
                  id:'0004',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
                  style:'background-image:url(https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png)',
                  time:'可订明日',
                  title:'故宫',
                  commentnum:32232,
                  price:60,
                  address:'东城区',
                  desc:'世界五大宫之首，穿越与您近在咫尺'
                },
                {
                  id:'0005',
                  imgUrl:'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
                  style:'background-image:url(https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png)',
                  time:'可订明日',
                  title:'故宫',
                  commentnum:32232,
                  price:60,
                  address:'东城区',
                  desc:'世界五大宫之首，穿越与您近在咫尺'
                },
              ]
            }
        }
    }
</script>

<style scoped lang="stylus">
  .favourite{
    margin-top: .2rem;
    background-color: #fff;
    .mp-border-bottom:before{
      position absolute
      bottom: 0
      left: 0
      display: block
      content :''
      height :1px
      width 100%
      border-bottom: 1px solid #e0e0e0;
      overflow: hidden;
      position: absolute;
    }
    .mp-group-title{
      position: relative;
      padding: .24rem 0 .26rem;
      img{
        display: inline-block;
        overflow: hidden;
        width: .3rem;
        height: .3rem;
        margin-left: .2rem;
        vertical-align: top;
      }
      span{
        display: inline-block;
        margin-left: .08rem;
        height: .44rem;
        color: #212121;
        font-size: .32rem;
        line-height: .44rem;
      }
    }
    .mp-like-list{
      margin-left: .24rem;
      .mp-like-item{
        position: relative;
        overflow: hidden;
        padding: .2rem 0;
      }
      .fulllink-img{
        float: left;
        overflow: hidden;
        width: 2rem;
        height: 2rem;
        img{
          width :100%
        }
      }

      .mp-like-tag{
        position: absolute;
        top: .2rem;
        left: 0;
        width: 1.02rem;
        height: .38rem;
        background-size: 100%;
        color: #fff;
        font-size: .2rem;
        line-height: .38rem;
        text-indent: .04rem;
      }
    }
    .mp-like-info{
      overflow: hidden;
      padding-left: .22rem
      .mp-like-title{
        margin-top: .26rem;
        height: .44rem;
        color: #212121;
        font-size: .32rem;
        line-height: .44rem;
      }
      .mp-ellipsis{
        overflow: hidden;
        width: 100%;
        white-space: nowrap;
        text-overflow: ellipsis;
      }
      .mp-like-comment{
        margin-top: .14rem;
        height: .34rem;
        .iconfont{
          width :0.24rem
          color #ffb436;
        }
        span{
          color: #616161;
          font-size: .24rem;
          line-height: .34rem;
          vertical-align: text-bottom;
        }
      }
      .mp-like-price{
        position: relative;
        margin-top: .22rem;
        color: #616161;
        font-size: .24rem;
        line-height: .4rem;
        .mpg-price{
          color: #ff8300;
          .mpg-price-num{
            font-size: .4rem;
          }
        }
        .mp-like-address{
          position: absolute;
          right: .24rem;
          bottom: 0;
        }
      }
      .mp-like-feature{
        display: inline-block;
        margin-top: .48rem;
        margin-right: .24rem;
        background: #fff9f9;
        padding: .04rem .1rem;
        color: #f55;
        font-size: .24rem;
        line-height: .34rem;
        .mp-ellipsis2{
          display: -webkit-box;
          overflow: hidden;
          text-overflow: ellipsis;
          -webkit-line-clamp: 2;
          -webkit-box-orient: vertical;
        }
      }
    }
    .mp-like-more{
      display: block;
      padding: .2rem 0;
      color: #00afc7;
      font-size: .28rem;
      line-height: .4rem;
      text-align: center;
    }
  }

</style>

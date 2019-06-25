<template>
   <div class="mp-promote">
     <slot></slot>
     <!--<h3 class="mp-ticket-type">去哪儿推荐</h3>-->
     <div class="mp-ticket-item" v-for="item in ticketList" :key="item.id">
       <div class="mp-ticket-main mp-flexbox-layout" >
         <div>
           <h6 class="mp-ticket-title mp-ellipsis2">{{item.desc}}</h6>
           <ul class="mp-ticket-light">
             <span class="mp-ticket-desctag">
               <img :src="item.imgUrl" alt=""
                    class="mp-ticket-tagicon">{{item.suimai}}
             </span>
           </ul>
           <ul class="mp-ticket-labelcon">
             <span class="mp-ticket-label mp-border mp-label14"><img
               src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png" alt=""
               class="mp-ticket-tagicon" v-if="item.ziying">{{item.ziying}}</span>
             <span class="mp-ticket-label mp-border mp-label14" v-if="item.huanpiao">{{item.huanpiao}}</span>
             <span class="mp-ticket-label mp-border mp-label14" v-if="item.tui">{{item.tui}}</span>
           </ul>
         </div>
       </div>
       <div class="mp-ticket-side mp-flexbox-layout">
         <a href="#"><strong class="mp-ticket-sale">￥<em class="mp-price-num">{{item.price}}</em></strong>
           <em class="downloadAppBtn">预定</em>
         </a>

       </div>
     </div>

   </div>
</template>

<script>
    export default {
        name: "DetailRecommend",
        data() {
            return {
              ticketList:[
                {
                  id:'0001',
                  imgUrl:'https://img1.qunarzz.com/piao/fusion/1804/94/3537f6969acc0c02.png',
                  desc:'【当日票】故宫成人票凭身份证入园（随买随用，快速入园）',
                  suimai:'16:00前随买随用',
                  ziying:'自营',
                  huanpiao:'无需换票',
                  tui:'条件退',
                  price:60
                },
                {
                  id:'0002',
                  imgUrl:'https://img1.qunarzz.com/piao/fusion/1804/94/3537f6969acc0c02.png',
                  desc:'【当日票】故宫成人票凭身份证入园（随买随用，快速入园）',
                  suimai:'16:00前随买随用',
                  ziying:'自营',
                  huanpiao:'无需换票',
                  tui:'条件退',
                  price:60
                },
                {
                  id:'0003',
                  imgUrl:'https://img1.qunarzz.com/piao/fusion/1804/94/3537f6969acc0c02.png',
                  desc:'【当日票】故宫成人票凭身份证入园（随买随用，快速入园）',
                  suimai:'16:00前随买随用',
                  ziying:'自营',
                  huanpiao:'',
                  tui:'条件退',
                  price:60
                },
              ]
            }
        }
    }
</script>

<style scoped lang="stylus">
 .mp-promote{
   position: relative;
   background: #fff;
   margin-bottom: .2rem;
   padding-left: .2rem;
   .mp-ticket-type{
     overflow: hidden;
     position: relative;
     z-index: 4;
     margin-bottom: -.02rem;
     padding: 0 .2rem;
     height: .88rem;
     background: #fff;
     color: #333;
     font-size: .32rem;
     line-height: .88rem;
     text-indent: .4rem;
     font-family: tahoma,arial,"Hiragino Sans GB","\5FAE\8F6F\96C5\9ED1",simsun,sans-serif;
   }
   .mp-ticket-item{
     padding: .2rem .2rem .24rem 0;
     box-sizing: border-box;
     display: flex;
     width: 100%;
     position: relative;
     .mp-ticket-main{
       -webkit-box-flex: 2.92;
       -moz-box-flex: 2.92;
       box-flex: 2.92;
       -webkit-flex: 2.92;
       -moz-flex: 2.92;
       -ms-flex: 2.92;
       flex: 2.92;

       .mp-ticket-title{
         margin-right: .1rem;
         line-height: .52rem;
         padding: 0;
         font-size: .3rem;
         color: #616161;
         display: -webkit-box;
         overflow: hidden;
         text-overflow: ellipsis;
         -webkit-line-clamp: 2;
         -webkit-box-orient: vertical;
       }
       .mp-ticket-light{
         overflow: hidden;
         .mp-ticket-desctag{
           display: inline-block;
           height: .32rem;
           color: #616161;
           font-size: .24rem;
           line-height: .32rem;
           white-space: nowrap;
           .mp-ticket-tagicon{
             display: inline-block;
             width: .2rem;
             max-height: .32rem;
             margin-right: .04rem;
             vertical-align: 0;
           }

         }

       }
       .mp-ticket-labelcon{
         font-size 0;
         .mp-ticket-label{
           display: inline-block;
           margin-top: .08rem;
           padding: 0 .04rem;
           height: .32rem;
           color: #00afc7;
           font-size: .2rem;
           line-height: .32rem;
           white-space: nowrap;
           position: relative;
           margin-right: .1rem;
           .mp-ticket-tagicon{
             display: inline-block;
             width: .2rem;
             max-height: .32rem;
             margin-right: .04rem;
             vertical-align: 0;
           }
         }
         .mp-ticket-label:before{
            display: block
           border: 1px solid #a5e4ec;
            /*border-color: #a5e4ec;*/
            border-radius: .08rem;
            width: 100%;
            height: 100%;
            box-sizing: border-box;
            top: 0;
            left: 0;
            content: " ";
            overflow: hidden;
            position: absolute;

          }
       }
     }
     .mp-flexbox-layout{
       display: flex;
       -ms-flex-align: center;
       -webkit-align-items: center;
       -webkit-box-align: center;
       align-items: center;
       width: .02rem;
     }
   }
  .mp-ticket-item:before{
    position absolute
    display: block
    content ''
    z-index: 1;
    border-color: #dadada;
    left: 0;
    width: 100%;
    height: 1px;
 }
   .mp-ticket-side{
     display: flex;
     -ms-flex-align: center;
     -webkit-align-items: center;
     -webkit-box-align: center;
     align-items: center;
     width: .02rem;
     flex 1
     a{
       box-sizing: border-box;
       display: block;
       width: 100%;
       padding-left: .2rem;
     }
     .mp-ticket-sale{
       display: block;
       overflow: hidden;
       font-size: .24rem;
       line-height: .28rem;
       text-align: center;
       color: #ff9800;
       height: .4rem;
       .mp-price-num{
         margin-left: .04rem;
         font-size: .4rem;
         text-align: center;
         line-height: .4rem;
         font:Tahoma,Helvetica,sans-serif;
       }
     }
     .downloadAppBtn{
       height: .6rem;
       color: #fff;
       font-size: .28rem;
       line-height: .6rem;
       -webkit-border-radius: .08rem;
       -moz-border-radius: .08rem;
       border-radius: .08rem;
       background-image: -webkit-gradient(linear,left top,right bottom,from(#ffab1e),to(#ff8c12));
       background-image: -webkit-linear-gradient(-60deg,#ffab1e 37%,#ff8c12 100%);
       background-image: -moz-linear-gradient(-60deg,#ffab1e 37%,#ff8c12 100%);
       background-image: -o-linear-gradient(-60deg,#ffab1e 37%,#ff8c12 100%);
       background-image: linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%);
       display: block;
       overflow: hidden;
       text-align center
     }
   }

 }
</style>

<template>
    <div class="mp-headfigure">

      <router-link to="/"><a href="#" class="mp-header-back">
        <span class="mp-headerback-bg"></span>
        <span class="iconfont icon-houtui"></span>
      </a></router-link>

      <div class="mp-headfigure-wrap">
        <img src="//img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg" alt="">
      </div>
      <div class="mp-headfeagure-info">
        <div class="mp-headfeagure-title">故宫(AAAAA景区)</div>
      </div>

    </div>
</template>

<script>
    export default {
        name: "DetailHead",
        data() {
            return {

            }
        },

    }
</script>

<style scoped lang="stylus">
 .mp-headfigure{
   position: relative;
   .mp-header-back{
     position: absolute;
     font-size: .36rem;
     color: #fff;
     text-align: center;
     left: .1rem;
     top: .1rem;
     width: .72rem;
     height: .72rem;
     line-height: .72rem;
     .mp-headerback-bg{
       display: block;
       width: .72rem;
       height: .72rem;
       background-color: #000;
       opacity: .5;
       -webkit-border-radius: .36rem;
       -moz-border-radius: .36rem;
       border-radius: .36rem;
     }
     .iconfont{
       position: absolute;
       left: 0;
       top: 0;
       display: block;
       width: .72rem;
       line-height: .72rem;
       text-align: left;
       text-indent: .2rem
     }
   }
   .mp-headfigure-wrap{
     overflow: hidden;
     height: 0;
     width: 100%;
     padding-bottom: 55%;
     img{
       width: 100%;
       vertical-align: top;
     }
   }
   .mp-headfeagure-info{
     position: absolute;
     right: .2rem;
     bottom: .36rem;
     left: .2rem;
     min-height: .4rem;
     .mp-headfeagure-title{
       position: relative;
       z-index: 1;
       line-height: .4rem;
       color: #fff;
       font-size: .36rem;
       text-shadow: 0 1px 2px rgba(0,0,0,0.70);
     }
   }

 }
</style>

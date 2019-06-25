<template>
  <div>
    <div class="mp-baseinfo">
      <div class="mpg-flexbox">
        <div class="mpg-flexbox-item">
          <div>
            <span class="mp-commentcard-score">5.0</span><span class="mp-commentcard-text">分</span><span class="mp-commentcard-desc">超赞</span>
          </div>
          <div>
            <span class="mp-totalcommentnum">413362条评论</span><span class="mp-totalcommentnum">93条攻略</span>
            <span class="iconfont icon-iconfontjiantou2"></span>
          </div>
        </div>
        <div class="mpg-flexbox-item item-before">
          <div>
            <span class="mp-sightcard-title">景点简介</span>
          </div>
          <div>
            <span class="mp-sightcard-text">开放时间、贴士</span>
            <span class="iconfont icon-iconfontjiantou2"></span>
          </div>
        </div>
      </div>
      <div class="mp-baseinfo-address">
        <p class="mp-baseinfo-address-txt">
          <span class="iconfont icon-dingwei"></span>北京市东城区景山前街4号
          <span class="iconfont icon-iconfontjiantou2"></span>
        </p>
      </div>
    </div>
    <div class="mp-announce-con">
      <div class="mp-announce-inner">
        <span class="iconfont icon-tongzhi"></span>1.如遇天安门广场戒严，请从故宫两侧（东华门或西华门），沿故宫城墙步行至午门验票！2.故宫博物院2019年延续周一闭馆（国家法定节假日除外）的措施，具体时间请以景区官方通知为准，给您带来不便敬请谅解。
        <span class="iconfont icon-iconfontjiantou2"></span>
      </div>
    </div>
  </div>

</template>

<script>
    export default {
        name: "BaseInfo",
        data() {
            return {}
        }
    }
</script>

<style scoped lang="stylus">
  .mp-baseinfo{
    position: relative;
    top: -.1rem;
    padding: .1rem .2rem 0 .2rem;
    margin-bottom: .1rem;
    background: #fff;
    -webkit-border-radius: .1rem .1rem 0 0;
    -moz-border-radius: .1rem .1rem 0 0;
    border-radius: .1rem .1rem 0 0;
    .mpg-flexbox{
      display: flex;
      width: 100%;
      padding-top: .1rem;
      padding-bottom: .2rem;
      .item-before:before{
        display block
        overflow: hidden;
        position: absolute;
        content ''
        top: 0;
        width: 1px;
        height: 100%;
        border-left: 1px solid #e0e0e0;
      }
      .mpg-flexbox-item{
        position: relative;
        flex 1;
        .mp-commentcard-score{
          font-size: .44rem;
          color: #ff8300;
          line-height: .44rem;
        }
        .mp-commentcard-text{
          font-size: .28rem;
          color: #ff8300;
          line-height: .48rem;
        }
        .mp-commentcard-desc{
          font-size: .28rem;
          color: #ff8300;
          line-height: .48rem;
          margin-left: .2rem;
        }
        .mp-totalcommentnum{
          font-size: .24rem;
          color: #9e9e9e;
          line-height: .32rem;
          margin-right: .2rem;
        }
        .iconfont{
          position: absolute;
          top: .3rem;
          right: .2rem;
          color: #9e9e9e;
          font-size: .24rem;
        }
        .mp-sightcard-title{
          font-size: .28rem;
          color: #212121;
          line-height: .48rem;
          padding-left: .3rem;
        }
        .mp-sightcard-text{
          color: #9e9e9e;
          font-size: .24rem;
          padding-left: .3rem;
        }
      }
    }
    .mp-baseinfo-address{
      display: block;
      position: relative;
      padding: .2rem 0;
      line-height: .36rem;
      color: #212121;
      .mp-baseinfo-address-txt{
        padding-right: .56rem;
        position: relative;
        padding-left: .56rem;
        .icon-dingwei{
          display: block;
          height: 100%;
          line-height: 100%;
          position: absolute;
          left: 0;
          top: .16rem;
          margin-top: -.16rem;
          margin-right: .2rem;
          color: #9e9e9e;
          font-size: .36rem;
        }
        .icon-iconfontjiantou2{
          position: absolute;
          right: 0;
          top: 50%;
          margin-top: -.14rem;
          color: #9e9e9e;
          font-size: .24rem;
        }

      }
    }
  }
    .mp-announce-con{
      background-color: #fff5e5;
      color: #ff8300;
      margin-bottom: .2rem;
      height: .88rem;
      line-height: .88rem;
      padding-left: .23rem;
      .mp-announce-inner{
        padding-right: .6rem;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        position: relative;
        .icon-tongzhi{
          color: #ff8300;
          margin-right: .1rem
        }
        .icon-iconfontjiantou2{
          right: .2rem;
          position: absolute;
          /*top: .3rem;*/
          color: gray;
        }
      }
    }

</style>

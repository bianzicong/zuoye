<template>
    <div class="footer">
      <div class="main_nav_wrapper">
        <ul class="main_nav">
          <li >
            <i class="iconfont icon-feiji"></i>
            <span class="title">机票</span>
          </li>
          <li >
            <i class="iconfont icon-jiudian"></i>
            <span class="title">酒店</span>
          </li>
          <li >
            <i class="iconfont icon-kezhangongyu"></i>
            <span class="title">公寓</span>
          </li>
          <li >
            <i class="iconfont icon-gengduo"></i>
            <span class="title">更多</span>
          </li>
        </ul>
        <ul class="footer_nav">
          <li>
            <a href="#">登录</a>
          </li>
          <li>
            <a href="#">我的订单</a>
          </li>
          <li>
            <a href="#">最近浏览</a>
          </li>
          <li>
            <a href="#">关于我们</a>
          </li>
        </ul>
        <ul class="mobile_pc">
          <li ><a href="#" class="choose">触屏版</a></li>
          <li><a href="#">电脑版</a></li>
        </ul>
        <div class="copyright">
          <span>Qunar 京ICP备05021087</span>
          <a href="#">意见反馈</a>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Footer",
        data() {
            return {}
        }
    }
</script>

<style scoped lang="stylus">
  .footer{
    background: #f3f3f3;
    .main_nav{
      position: relative;
      width: 300px;
      height: 25px;
      margin: 0 auto;
      padding: 10px 10px 0 10px;
      overflow: hidden;
      li{
        margin: 0px;
        padding-left: 10px;
        height: 31px;
        width: 65px;
        float: left;
        position: relative;
        background: none;
        .iconfont{
          color: #9e9e9e;
        }
        .title{
          display: inline-block;
          color: #9e9e9e;

          border-bottom: 1px solid #acacac;
          font-size: 12px;
        }

      }



    }
    .footer_nav{
      width: 100%;
      height: 39px;
      border-bottom: 1px solid #cacaca;

      li{
        float: left;
        padding-left: 20px;
        .choose:active{
          color :black
        }
        a{
          position: relative;
          color: #25a4bb;
          font-size: 14px;
          line-height: 39px;
        }
      }
    }
    .mobile_pc{
      padding: 10px 0 0 0;
      text-align: center;
      li{
        display: inline-block;
        margin: 0 15px;
      }
      .choose{
        color black;
      }
    }
    .copyright{
      color: #9e9e9e;
      text-align: center;
      font-size: 14px;
      padding: 10px;
      span{
        color: #9e9e9e;
        text-align: center;
        font-size: 14px;
      }
      a{
        color: #9e9e9e;
      }

    }
  }
</style>

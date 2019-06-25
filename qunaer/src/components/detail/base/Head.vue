<template>
    <div class="head">
      <div class="header-fixed" v-show="!isShow" :style="styleObj">
        <router-link to="/"><i class="iconfont icon-houtui"></i></router-link>

        <h1 class="mp-header-title">故宫</h1>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Head",
        data() {
            return {
              isShow:true,
              styleObj:{}
            }
        },
      methods:{
        handleScroll(){
          let scrollTop=document.documentElement.scrollTop;
          if (scrollTop>40){
            this.isShow=false;
            this.styleObj={
              opacity:(scrollTop-40)/100
            }
          } else {
            this.isShow=true;
          }
          // console.log(document.documentElement.scrollTop)
        }
      },
      activated(){
        window.addEventListener('scroll',this.handleScroll)
      },
      deactivated(){
          window.removeEventListener('scroll',this.handleScroll)
      }
    }
</script>

<style scoped lang="stylus">
.head{

  .header-fixed{
    height: .88rem;
    background: #00bcd4;
    z-index: 91;
    position: fixed;
    width: 100%;
    top: 0px;
    left: 0px;
    display: block;
    opacity: 1;
    .iconfont{
      left: 0;
      top: 0;
      width: .8rem;
      height: .88rem;
      line-height: .88rem;
      position: absolute;
      font-size: .36rem;
      color: #fff;
      text-align: center;
    }
    .mp-header-title{
      overflow: hidden;
      margin: 0 1rem;
      line-height: .88rem;
      white-space: nowrap;
      text-overflow: ellipsis;
      font-size: .32rem;
      text-align: center;
      color: #fff;
    }
  }
}
</style>

<template>
 <div class="header">
    <i class="iconfont icon-houtui header-back"></i>
   <div class="header-input">
     <i class="iconfont icon-xiazai17"></i>
     <input type="text" placeholder="输入城市/景点/游玩主题">
   </div>
   <div class="header-right">
      <span>厦门</span><i class="iconfont icon-htmal5icon03"></i>
   </div>
 </div>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return {

    }
  }
}
</script>

<style lang="stylus" scoped>
  .header{
    display flex;
    height :.88rem;
    background-color: #00bcd4;
    line-height :.88rem;
    color :#fff;
    .header-back{
      width :.88rem;
      text-align :center;
    }
    .header-input{
      flex:1;
      background-color: #fff;
      line-height :.60rem;
      height :.60rem;
      padding-left :.1rem;
      margin-top:.12rem;
      border-radius :.1rem;
      .icon-xiazai17{
        color :#ccc;
        vertical-align :middle
      }
      input{
        width: 80%;
        vertical-align :middle
        font-size :.24rem;
        color :#e4e7ea;
      }
    }
    .header-right{
      padding:0 .2rem;
      span{
        vertical-align :7%;
      }
      .icon-htmal5icon03{
        font-size :.24rem;
        vertical-align :12%;
      }
    }
  }

</style>

<template>
  <div class="detail">
    <detail-head></detail-head>
    <base-info></base-info>
    <keep-alive>
      <head-scoll></head-scoll>
    </keep-alive>
    <detail-recommend>
      <h3 class="mp-ticket-type">去哪儿推荐</h3>
    </detail-recommend>
    <calendar></calendar>
    <home-footer></home-footer>
  </div>
</template>

<script>
  import DetailHead from './base/DetailHead'
  import BaseInfo from './base/BaseInfo'
  import HeadScoll from './base/Head'
  import DetailRecommend from './base/DetailRecommend'
  import Calendar from './base/Calendar'
  import HomeFooter from '../home/base/Footer'
    export default {
        name: "Detail",
        data() {
            return {}
        },
        components:{
          DetailHead,
          BaseInfo,
          HeadScoll,
          DetailRecommend,
          Calendar,
          HomeFooter
        },
        created(){
          document.documentElement.scrollTop=0;
        }
    }
</script>

<style scoped lang="stylus">
  .detail{

  }
</style>

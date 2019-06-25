<template>
  <div class="swiper">
    <swiper :options="swiperOption" ref="mySwiper" v-if="swiperList.length>0">
      <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>

      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>

</template>

<script>
  import 'swiper/dist/css/swiper.css'
  import { swiper, swiperSlide } from 'vue-awesome-swiper'
    export default {
        name: "Swiper",
        data() {
        return {
          swiperOption: {
            pagination: {
              el: '.swiper-pagination',

            },
            autoplay : {
              disableOnInteraction: false, //用户操作后是否禁止自动循环
              delay: 3000 //自自动循环时间
            },
            loop:true
          },
          swiperList:[
            {
              id:'0001',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/667757f979fa38b12c4986f9930b6695.jpg_750x200_6cca7add.jpg'
            },
            {
              id:'0002',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/d7bbc21db442366a882e04ddc984669a.jpg_750x200_85e640d9.jpg'
            },
            {
              id:'0003',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
            },
            {
              id:'0004',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/b48d1ce6662a905d993635b4e28ff089.jpg_750x200_1c00b2f0.jpg'
            },
            {
              id:'0005',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/025aaafa0fc7828dbc87bbbd8f065eff.jpg_750x200_c8e29266.jpg'
            },
            {
              id:'0006',
              imgUrl:'http://img1.qunarzz.com/piao/fusion/1701/c6/ffde478b37201002.jpg_750x200_4315dcea.jpg'
            },
          ]
        }
      },
      computed: {
        swiper() {
          return this.$refs.mySwiper.swiper
        }
      },
      mounted() {

      },

      components:{
        swiper,
        swiperSlide
      }
    }
</script>

<style scoped lang="stylus">
  .swiper>>>.swiper-pagination-bullet-active{
    background: #fff;
  }
    .swiper>>>.swiper-pagination-bullet{
      width :6px;
      height :6px
    }
  .swiper{
    height :2rem;
    .swiper-container{
      height :100%;
    }
    .swiper-img{
      width:100%;
      height :100%;
    }

  }
</style>

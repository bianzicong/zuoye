<template>
    <div class="nav-content">
      <swiper :options="swiperOption" ref="mySwiper">
        <!-- slides -->
        <swiper-slide v-for="imgs in filterImgs" >
          <div class="nav">
            <div class="item"  v-for="item in imgs" :key="item.id">
              <img class="item-img" :src="item.imgUrl" alt="">
              <span class="item-desc">{{item.desc}}</span>
            </div>
          </div>
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
      <div class="choose">
        <div class="dingwei"><i class="iconfont icon-dingwei"></i>定位失败</div>
        <div class="biyou"><i class="iconfont icon-diqiuquanqiu"></i>必游榜单</div>
      </div>
    </div>
</template>

<script>
  import 'swiper/dist/css/swiper.css'
  import { swiper, swiperSlide } from 'vue-awesome-swiper'
    export default {
        name: "Nav",
        data() {
            return {
              swiperOption: {
                pagination: {
                  el: '.swiper-pagination',

                },
              },
              imgList:[{
                'id':'0001',
                'imgUrl':'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                'desc':'景点门票'
              },
                {
                  'id':'0002',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                  'desc':'一日游'
                },
                {
                  'id':'0003',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                  'desc':'厦门必游'
                },
                {
                  'id':'0004',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1803/97/02f5043b51b2102.png',
                  'desc':'鼓浪屿'
                },
                {
                  'id':'0005',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
                  'desc':'武夷山'
                },
                {
                  'id':'0006',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
                  'desc':'动植物园'
                },
                {
                  'id':'0007',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
                  'desc':'景点门票'
                },
                {
                  'id':'0008',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
                  'desc':'展馆展览'
                },
                {
                  'id':'0009',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png',
                  'desc':'游船观光'
                },
                {
                  'id':'0010',
                  'imgUrl':'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
                  'desc':'水上乐园'
                }
              ]
            }
        },
        computed:{
          filterImgs(){
            let imgs=[]
            this.imgList.forEach((item,index)=>{
              let page = ~~(index/8)
              if (!imgs[page]){
                imgs[page]=[]
              }
              imgs[page].push(item)
            })
            return imgs;
          }
        },
      components:{
        swiper,
        swiperSlide
      }
    }
</script>

<style scoped lang="stylus">


.swiper-pagination{
  bottom:0.05rem;
}
.swiper>>>.swiper-pagination-bullet{
  width :6px;
  height :6px
}
  .nav-content{
    background-color: #fff;
  }
.nav{
  display: flex;
  flex-wrap: wrap;
  height :3.8rem;
  /*background-color: pink;*/
  .item{
    display: flex;
    flex-direction: column;
    align-items :center;
    text-align :center;
    width :25%;
    height:50%;
    .item-img{
      width :1.1rem;
      margin-top:.2rem;
    }
  }
}
  .choose{
    display: flex
    width :100%;
    height :0.98rem;
    /*background-color: pink;*/
    line-height :0.98rem;
    text-align :center;
    border-top:0.01rem solid #eaeaea;
    .dingwei{
      width :50%
      border-right :0.01rem solid #eaeaea;
    }
    .dingwei:after{
      content :""
      height:100%;
      width :0.01rem;
      background-color: #eaeaea;
    }
    .biyou{
      width 50%

    }
  }
</style>

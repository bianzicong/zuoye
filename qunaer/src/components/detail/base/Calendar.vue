<template>
  <div>
    <div class="mpw-calendar-tabout">
      <div class="mp-border-bottom">
        <span class="mpw-calendar-tabitem">门票</span>
        <span class="mpw-calendar-tabitem">一日游</span>
        <span class="mpw-calendar-tabitem">景区服务</span>
        <span class="mpw-calendar-tabitem">热销组合</span>
      </div>
      <div class="mp-tab-slider"></div>
    </div>
    <div v-for="item in shopList" :key="item.id">
      <div class="mp-ticket-group" >
        <h3 class="mp-ticket-type">
          <span>{{item.title}}</span>
        </h3>
        <div class="mp-ticket-list" v-for="ticket in item.ticket" :key="ticket.id">
          <div class="mp-ticket-type-info">
            <h5 class="mp-ticket-type-name">{{ticket.desc}}</h5>
            <div class="mp-ticket-type-price">￥
              <em class="mp-price-num">{{ticket.price}}</em>
              <span class="mp-ticket-numword">起</span>
            </div>
            <i class="iconfont icon-tubiao-"></i>
          </div>
        </div>
        <div class="mp-more-refresh">
          查询剩余产品<i class="iconfont icon-tubiao-"></i>
        </div>
      </div>
    </div>

  </div>

</template>

<script>
    export default {
        name: "Calendar",
        data() {
            return {
              shopList:[
                {
                  id:'0001',
                  title: '故宫当日票',
                  ticket:[
                    {
                      id:'0001',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                    {
                      id:'0002',

                      desc:'【当日票】故宫成人票',
                      price:60
                    }
                  ]
                },
                {
                  id:'0002',
                  title: '故宫当日票',
                  ticket:[
                    {
                      id:'0001',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                    {
                      id:'0002',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                  ]
                },
                {
                  id:'0003',
                  title: '故宫当日票',
                  ticket:[
                    {
                      id:'0001',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                    {
                      id:'0002',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                  ]
                },
                {
                  id:'0004',
                  title: '故宫当日票',
                  ticket:[
                    {
                      id:'0001',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                    {
                      id:'0002',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                  ]
                },
                {
                  id:'0005',
                  title: '故宫当日票',
                  ticket:[
                    {
                      id:'0001',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                    {
                      id:'0002',

                      desc:'【当日票】故宫成人票',
                      price:60
                    },
                  ]
                },
              ]
            }
        }
    }
</script>

<style scoped lang="stylus">
  .mpw-calendar-tabout{
    position: relative;
    background-color: #fff;
    color: #212121;
    height: .96rem;
    line-height: .96rem;
    white-space: nowrap;
    overflow-x: auto;
    .mp-border-bottom{
      width: 8.2rem;
      position: relative;
      .mpw-calendar-tabitem{
        width: 2rem;
        display: inline-block;
        height: .92rem;
        line-height: .96rem;
        text-align: center;
        font-size: .32rem;
      }
    }
    .mp-tab-slider{
      position: absolute;
      bottom: 0;
      left: 15px;
      display: inline-block;
      height: .04rem;
      width: 1.4rem;
      background-color: #00bcd4;
    }

  }

  .mpw-calendar-tabout:before{
    content: " ";
    overflow: hidden;
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 1px;
    border-bottom: 1px solid #e0e0e0;
  }
  .mp-ticket-group{
    margin-bottom: .2rem;
    background: #fff;
    position: relative;
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
    }
  .mp-ticket-type:before{
    content: " ";
    overflow: hidden;
    position: absolute;
    left: .2rem;
    bottom: 0;
    width: 100%;
    height: 1px;
    border-bottom: 1px solid #dadada;
  }
    .mp-ticket-list{
      overflow: hidden;
      position: relative
      .mp-ticket-type-info{
        position: relative;
        z-index: 2;
        margin-bottom: -.02rem;
        padding: .24rem .2rem;
        background: #fff;
        .iconfont{
          right: .2rem;
          margin-top: -.22rem;
          color: #bbb;
          font-size: .24rem;
          overflow: hidden;
          position: absolute;
          top: 50%;
          height: .4rem;
          line-height: .4rem;
        }
        .mp-ticket-type-name{
          margin-right: 1.8rem;
          color: #333;
          font-size: .3rem;
          line-height: .48rem;
          display: -webkit-box;
          overflow: hidden;
          text-overflow: ellipsis;
          -webkit-line-clamp: 2;
          -webkit-box-orient: vertical;
        }
        .mp-ticket-type-price{
          right: .46rem;
          margin-top: -.28rem;
          color: #ff9800;
          overflow: hidden;
          position: absolute;
          top: 50%;
          height: .4rem;
          line-height: .4rem;
          font: .24rem "Microsoft yahei","Hiragino sans gb",Arial,sans-serif;
          .mp-price-num{
            margin-left: .04rem;
            font-size: .38rem;
            font:Tahoma,Helvetica,sans-serif;
          }
          .mp-ticket-numword{
            display: inline-block;
            color: #9e9e9e;
            font-size: .24rem;
            -webkit-transform: scale(.8);
            -moz-transform: scale(.8);
            -ms-transform: scale(.8);
            -o-transform: scale(.8);
            transform: scale(.8);
            line-height .4rem

          }

        }
      }
    }
  .mp-ticket-list:before{
    content: " ";
    overflow: hidden;
    position: absolute;
    left: 0rem;
    bottom: 0;
    width: 100%;
    height: 1px;
    z-index 3
    border-bottom: 1px solid #dadada;
  }
  }
  .mp-ticket-group:before{
    content: " ";
    overflow: hidden;
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 1px;
    border-bottom: 1px solid #e0e0e0;
  }
  .mp-more-refresh{
    position: relative;
    margin-top: -.02rem;
    height: .8rem;
    background: #fff;
    color: #616161;
    line-height: .8rem;
    text-align: center;
    z-index: 2;
    .iconfont{
      margin-left: .1rem;
      color: #616161;
      font-size: .2rem;
    }
  }
  .mp-more-refresh:before{
    content: " ";
    overflow: hidden;
    position: absolute;
    left: .2rem;
    bottom: 0;
    width: 100%;
    height: 1px;
    border-bottom: 1px solid #dadada;
  }
</style>

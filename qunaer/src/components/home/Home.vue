<template>
 <div class="class">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-nav></home-nav>
    <hot></hot>
    <home-favourite></home-favourite>
    <home-weekend></home-weekend>
    <home-footer></home-footer>
 </div>
</template>

<script>
import HomeHeader from './base/Header'
import HomeSwiper from './base/Swiper'
import HomeNav from './base/Nav'
import HomeFavourite from './base/Favourite'
import Hot from './base/Hot'
import HomeWeekend from './base/Weekend'
import HomeFooter from './base/Footer'
export default {
  name: 'home',
  components:{
    HomeHeader,
    HomeSwiper,
    HomeNav,
    HomeFavourite,
    Hot,
    HomeWeekend,
    HomeFooter
  }
}
</script>

<style scoped>

</style>

<template>
<div class="swiper">
  <swiper :options="swiperOption" >
    <swiper-slide v-for="item of imgList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      imgList: [{
        id: '001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/472a476c776c6fd962fcfd6fd75521d5.jpg_750x200_298bac66.jpg'
      },
      {
        id: '002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/5f6eaa320a5e9bc02e6ab12ba3c2841a.jpg_750x200_291d4dad.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.swiper >>> .swiper-pagination-bullet-active
  background: #fff
.swiper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 26.7%
  background: #eee
  .swiper-img
    width: 100%

</style>

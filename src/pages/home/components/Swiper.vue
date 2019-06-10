<template>
<div class="swiper" :options="swiperOption">
  <swiper  >
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
        loop: true,
        pagination: '.swiper-pagination'
      },
      imgList: [{
        id: '001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/472a476c776c6fd962fcfd6fd75521d5.jpg_750x200_298bac66.jpg'
      },
      {
        id: '002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/5f6eaa320a5e9bc02e6ab12ba3c2841a.jpg_750x200_291d4dad.jpg'
      },
      {
        id: '003',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/aef5f8864f5a1167599609307571b2c4.jpg_750x200_db7bedbe.jpg'
      },
      {
        id: '004',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/6ab65be3878a5ea365514cf3a8125fd1.jpg_750x200_7b2fe404.jpg'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.swiper >>> .swiper-pagination-bullet-active
  background: red
.swiper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 26.7%
  background: #eee
  .swiper-img
    width: 100%

</style>

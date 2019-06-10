<template>
<div class="swiper" :options="swiperOption">
  <swiper  >
    <swiper-slide v-for="item of list" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>

</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        loop: true,
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
.swiper >>> .swiper-pagination-bullet-active
  background: blue
.swiper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 26.7%
  background: #eee
  .swiper-img
    width: 100%

</style>

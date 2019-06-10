<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div  class="icon-img" >
            <img class="icon-image" :src="item.imgUrl" />
          </div>
          <div class="icon-des">{{item.iconDes}}</div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        loop: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }

  }
}
</script>
<style lang="stylus" scoped>
.icons >>> .swiper-pagination-bullets-active
  background: blue
.icons >>> .swiper-pagination-bullets
  bottom: -2px
.icons
  overflow: hidden
  height: 0
  padding-bottom: 52%
  .icon
    position: relative
    float: left
    width: 25%
    height: 0
    padding-bottom: 25%
    .icon-img
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: 22 px
      box-sizing: border-box
      padding: 5 px
      .icon-image
        height: 100%
        display: block
        margin: 0 auto
    .icon-des
      width: 100%
      position: absolute
      bottom: 0
      line-height: 22 px
      height: 22 px
      text-align: center
      color: #212121

</style>

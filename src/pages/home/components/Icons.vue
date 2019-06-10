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
  data () {
    return {
      swiperOption: {
        loop: false,
        pagination: '.swiper-pagination'
      },
      iconList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        iconDes: '景点门票'
      },
      {
        id: '002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/f0f00d6dfe038c044dbc9a437f58b0eb.png',
        iconDes: '一日游'
      },
      {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        iconDes: '北京必游'
      },
      {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
        iconDes: '水上乐园'
      },
      {
        id: '005',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/0334cf5430b9b5505fd79e2b8d7e8670.png',
        iconDes: '爬长城'
      },
      {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
        iconDes: '故宫'
      },
      {
        id: '007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        iconDes: '动植物园'
      },
      {
        id: '008',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/35d83bb968d80d54926f30cfb92cb6ff.png',
        iconDes: '限时抢购'
      },
      {
        id: '009',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/b4511345827006994aa1980a3886f0ac.png',
        iconDes: '世博园'
      },
      {
        id: '010',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/338c5b924c5809e8c7b14f60a953c3e2.png',
        iconDes: '欢乐谷'
      }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
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

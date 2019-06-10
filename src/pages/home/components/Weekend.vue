<template>
  <div class="recommend">
    <div class="recommend-title">  周末游</div>
    <ul>
      <li class="item border-bottom" v-for="item of itemList" :key="item.id">
         <div class="item-img-wraper">
           <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.itemTitle}} </p>
          <p class="item-desc">{{item.itemDesc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      itemList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
          itemTitle: '北京故宫博物馆',
          itemDesc: '世界最大的皇家博物馆，历史悠久'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/7e/476589267ebb41.jpg_r_640x214_bf599709.jpg',
          itemTitle: '北京欢乐谷',
          itemDesc: '世界最大的欢乐谷，历史悠久'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
          itemTitle: '八达岭长城',
          itemDesc: '世界最长的长城，历史悠久'
        },
        {
          id: '004',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
          itemTitle: '北京动物园',
          itemDesc: '世界上动物最多的动物园，历史悠久'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.recommend-title
  margin-top: .2 rem
  line-height: 1.8 rem
  background: #eee
  text-indent: .2 rem
.item-img-wraper
  margin-top: .4 rem
  overflow: hidden
  height: 0
  padding-bottom: 33.9%
  .item-img
    width: 100%

.item-info
  padding: 5px
  .item-title
    ellipsis()
    min-width: 0
    line-height: 25px
    fontsize: 16px
  .item-desc
    ellipsis()
    line-height: 20 px
    color: #ccc

</style>

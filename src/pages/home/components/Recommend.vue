<template>
  <div class="recommend">
    <div class="recommend-title">  热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of itemList" :key="item.id">
         <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.itemTitle}} </p>
          <p class="item-desc">{{item.itemDesc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      itemList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
          itemTitle: '北京故宫博物馆',
          itemDesc: '世界最大的皇家博物馆，历史悠久'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
          itemTitle: '北京欢乐谷',
          itemDesc: '世界最大的欢乐谷，历史悠久'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_200x200_2458ffb2.jpg',
          itemTitle: '八达岭长城',
          itemDesc: '世界最长的长城，历史悠久'
        },
        {
          id: '004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201308/08/41150dacc0e3a0c8c8d65eac.jpg_200x200_c62292e9.jpg',
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
.recommend
   margin-top: 1.2 rem
  .recommend-title
    margin-top: .2 rem
    line-height: 1.8 rem
    background: #eee
    text-indent: .2 rem
  .item
    overflow hidden
    display: flex
    height: 94 px
    .item-img
      width: 84 px
      height: 84px
      padding: 5px
    .item-info
      flex: 1
      padding: 5px
      min-width: 0
      .item-title
        ellipsis()
        min-width: 0
        line-height: 25px
        fontsize: 16px
      .item-desc
        ellipsis()
        line-height: 20 px
        color: #ccc
      .item-button
        line-height: 22px
        margin-top: 8 px
        color: #fff
        background: #ff9300
        padding: 0 10 px
        border-radius: 3px
</style>

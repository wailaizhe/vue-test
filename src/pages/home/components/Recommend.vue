<template>
  <div class="recommend">
    <div class="recommend-title">  热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
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
  props: {
    list: Array
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

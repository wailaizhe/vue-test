<template>
  <div class="recommend">
    <div class="recommend-title">  周末游</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
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
  props: {
    list: Array
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
  padding-bottom: 37%
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

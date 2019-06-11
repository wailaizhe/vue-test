<template>
<div class="header">
  <div class="header-left">
    <div class="iconfont back-icon">&#xe606;</div>
  </div>
  <div class="header-input">
     <span class="iconfont">&#xe614;</span>
     输入城市/景点/游玩主题
  </div>
  <router-link to="/city">
    <div class="header-right">
      {{city}}
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </router-link>
</div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/variable.styl'
  .header
    display: flex
    line-height: 43 px
    background: $bgColor
    color: #fff
    .header-left
      width: 40 px
      float: left
      margin-left: 5 px
      .back-icon
        text-agein: center
        fontsize: 20 px
    .header-input
      padding-left: 5 px
      flex: 1
      background: #ffffff
      border-radius: 5px
      margin-top: 4px
      margin-left: 4px
      line-height: 33px
      height: 33px
      color:#ccc
    .header-right
      width: 62 px
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        font-size: 12 px
        margin-left: -4 px
</style>

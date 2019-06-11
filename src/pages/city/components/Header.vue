<template>
  <div class="city-header">
    城市选择
    <router-link to = "/">
      <div class="iconfont header-back"> &#xe606; </div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
@import '~styles/variable.styl'
.city-header
  position: relative
  overflow: hidden
  line-height: 43 px
  background: $bgColor
  text-align: center
  color: #fff
  .header-back
    top: 0
    left: 0
    width: 30 px
    position: absolute
    fontsize: 20 px
    color: #fff
</style>

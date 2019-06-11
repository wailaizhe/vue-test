<template>
  <div class="city-search">
    <input class="search-input" type="text" placeholder="请输入城市名或拼音" />
  </div>
</template>
<script>
export default {
  name: 'CitySearch'
}
</script>
<style lang="stylus" scoped>
@import '~styles/variable.styl'
.city-search
  background: $bgColor
  padding: 0 8px
  height: 38 px
  .search-input
    height: 28 px
    width: 100%
    left: 4px
    line-height: 26px
    text-align: center
    border-radius: 3px
    color: #666
</style>

<template>
  <div class="header">
   <div class="left"><div class="iconfont fanhui">&#xe624;</div></div><!--iconfont类要写才能显示成功-->
   <div class="input"><span class="iconfont ">&#xe632;</span>输入城市/景点/游玩</div>
   <div class="right">城市<span class="iconfont">&#xe6aa;</span></div>
  </div>
</template>
 <script>
export default {
  name: "Header1",
};
</script>
<style lang="stylus" scoped>//1rem=50px 1px=0.02rem     css样式中@需在前面用~
@import '~@/assets/styles/stylus1.styl'
.header
  height:0.86rem
  line-height:0.86rem
  display:flex
  background :$bgcolor
  color :#fff
  .left
    width :.64rem
    float:left
    .fanhui
      font-size .4rem
      text-align center
  .input
    flex:1
    background :white
    height :.62rem
    line-height :.62rem
    margin-top:.12rem
    margin-left:.2rem
    padding-left:.2rem
    border-radius .1rem
    color #ccc
  .right
    width :1.24rem
    float:right
    text-align :center

  


</style>




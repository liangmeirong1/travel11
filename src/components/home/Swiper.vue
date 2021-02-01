<template>
  <div class="recommendPage">
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide v-for="item in list" :key="item.id"
        ><img :src="item.url"
      /></swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
// 引入插件
import { swiper, swiperSlide } from "vue-awesome-swiper";
import "swiper/dist/css/swiper.css";

export default {
  name: "Swiper",
  components: {
    swiper,
    swiperSlide,
  },
  data() {
    return {
      list: [
        {
          id: "1",
          url:
            "https://imgs.qunarzz.com/vc/e2/71/ae/263f464182ae2defed78fb9247.jpg_224x85x92.jpg",
        },
        {
          id: "2",
          url:
            "https://imgs.qunarzz.com/vc/46/f4/3f/6b2a07667356cba1f3901ce774.jpg_224x85x92.jpg",
        },
        {
          id: "3",
          url:
            "https://imgs.qunarzz.com/vc/52/87/17/3b7d4dfee3e56e31c66ab363d8.jpg_224x85x92.jpg",
        },
      ],
      swiperOption: {
        loop: true,
        autoplay: {
          delay: 1000,
          stopOnLastSlide: false,
          disableOnInteraction: false,
        },
        // 显示分页
        pagination: {
          el: ".swiper-pagination",
          clickable: true, //允许分页点击跳转
        },
      },
    };
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.swiper;
    },
  },
};
</script>
<style lang='stylus' scoped >
.recommendPage >>> .swiper-pagination-bullet-active
  background #fff
.recommendPage
  background #ccc
  overflow hidden
  width 100%
  height 0
  padding-bottom 38% // 相对width的38%,因为是图片的高宽比，或者给高度为 height 38vw
  .swiper-container
    position relative
    width 100%
    .swiper-slide
      width 100%
      img
        width 100%
</style>
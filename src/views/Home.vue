<template>
  <div id="app">
    <header1/>
    <swiper/>
  </div>
</template>
 <script>

import Header1 from '../components/home/Header1.vue';
import Swiper from '../components/home/Swiper.vue';
export default {
  name: "Home",
  components: {Header1,Swiper},
};
</script>
<template>
<div class="qwer">
    <swiper :options="swiperOption" ref="mySwiper">
    <swiper-slide >
      <img src = "@/assets/img/1.jpg" >
    </swiper-slide>
    <swiper-slide >
      <img src = "../assets/img/2.jpg" >
    </swiper-slide>
    <swiper-slide v-for="(image, index) in imgages" :key="index">
      <img :src="image" alt="">
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
    <div class="swiper-button swiper-button-prev" slot="button-prev">
    </div>
    <div class="swiper-button swiper-button-next" slot="button-next">
    </div>
  </swiper>
</div>
  
</template>

<script>
import "swiper/dist/css/swiper.css";
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  name: "Slider",
  data() {
    return {
      swiperOption: {
        pagination: {
          el: ".swiper-pagination",
          type: "fraction"
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      },
      imgages: []
    };
  },
  components: {
    swiper,
    swiperSlide
  },
  computed: {

  },

};
</script>

<style scoped >
img {
  width: 100%;
}
.qwer {
  height: 83vh;
  background: rgba(0, 0, 0, .2px)
}
/* .qwer::after {
    position: absolute;
    z-index: 999;
    width: 80%;
    content: "";
    bottom: 0;
    background: rgba(0,0,0,.7);
    height: 85%;
} */
.swiper-container {
  height: 100%;
}
</style>


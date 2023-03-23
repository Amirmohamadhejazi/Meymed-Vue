<template>
  <h1>sec 4 </h1>
  <div class="w-100" >
    <swiper :modules="[Virtual]" :slides-per-view="4"     >
      <swiper-slide
          v-for="items in itemsSwipe"
          :key="items.id"
          :virtualIndex="items.id"
      >
        <cardItemsShop :dataCard="items"/>
      </swiper-slide>
    </swiper>

  </div>
</template>


<style>
/************************************ Box ****************************************/
.swiper-slide {
  width: auto!important;
  margin: 0 12px 0 12px;
  cursor: pointer;
}
.swiper-container {
  display: flex;
  justify-content: center!important;
  align-items: center!important;
}
/************************************ Box ****************************************/
@media only screen and (max-width: 1199px) {

}
@media only screen and (max-width: 767px) {

}
@media only screen and (max-width: 500px) {

}
@media only screen and (max-width: 575px) {

}
</style>

<script>

import {Swiper, SwiperSlide} from "swiper/vue";
import {Virtual} from "swiper";
import cardItemsShop from "../helperComponents/cardItemsShop.vue";
import img1 from "../../assets/img/icon/sec2/sec2iconitems1.svg"
import img2 from "../../assets/img/icon/sec2/sec2iconitems2.svg"
import img3 from "../../assets/img/icon/sec2/sec2iconitems3.svg"
import img4 from "../../assets/img/icon/sec2/sec2iconitems4.svg"

export default {
  data() {
    return {
      number_option: 0,
      itemsSwipe: [
        {
          img:img4,
          title:"کد 84514",
          description:"تب سنج دیجیتال رز دیتا",
          price:45000,
          percentage:0,
          id:0
        },
        {
          img:img3,
          title:"کد 81544",
          description:"تب سنج دیجیتال رز دیتا",
          price:68479,
          percentage:0,
          id:1
        },
        {
          img:img2,
          title:"کد 823014",
          description:"تب سنج دیجیتال رز دیتا",
          price:547920,
          percentage:10,
          id:2
        },
        {
          img:img1,
          title:"کد 81774",
          description:"تب سنج دیجیتال رز دیتا",
          price:390000,
          percentage:6,
          id:3
        },
        {
          img:img4,
          title:"کد 84514",
          description:"تب سنج دیجیتال رز دیتا",
          price:45000,
          percentage:0,
          id:4
        },
        {
          img:img3,
          title:"کد 81544",
          description:"تب سنج دیجیتال رز دیتا",
          price:68479,
          percentage:0,
          id:5
        },
        {
          img:img2,
          title:"کد 823014",
          description:"تب سنج دیجیتال رز دیتا",
          price:547920,
          percentage:10,
          id:6
        },
        {
          img:img1,
          title:"کد 81774",
          description:"تب سنج دیجیتال رز دیتا",
          price:390000,
          percentage:6,
          id:7
        },
        {
          img:img4,
          title:"کد 84514",
          description:"تب سنج دیجیتال رز دیتا",
          price:45000,
          percentage:0,
          id:8
        },
        {
          img:img3,
          title:"کد 81544",
          description:"تب سنج دیجیتال رز دیتا",
          price:68479,
          percentage:0,
          id:9
        },
        {
          img:img2,
          title:"کد 823014",
          description:"تب سنج دیجیتال رز دیتا",
          price:547920,
          percentage:10,
          id:10
        },
        {
          img:img1,
          title:"کد 81774",
          description:"تب سنج دیجیتال رز دیتا",
          price:390000,
          percentage:6,
          id:11
        },
      ]
    }
  },

  components:{
    Swiper,
    SwiperSlide,
    cardItemsShop
  },
  setup() {
    // const slides = Array.from({ length: 10 }).map(
    //     (el, index) => `Slide ${index + 1}`
    // );
    return {
      // slides,
      Virtual,
    };
  },
  mounted() {
    // Initialize Swiper.js instance
   },



}
</script>

<template>
  <div>
    <swiper :modules="[Virtual]" :slides-per-view="3" :space-between="20" virtual  loop >
      <swiper-slide
          v-for="(slideContent, index) in slides"
          :key="index"
          :virtualIndex="index"
      >{{slideContent}}</swiper-slide
      >

  </swiper>

  </div>

</template>
<script>
import { Virtual , Thumbs } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  props: {
  },
  mounted() {
    // Access slot props data using $slots.default().props
    console.log(this.$slots.default()[0].props)
  },

  setup() {
    const slides = Array.from({ length: 10 }).map(
        (el, index) => `Slide ${index + 1}`
    );
    return {
      slides,
      Virtual,
    };
  },
};
</script>
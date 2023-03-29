<template>
  <div class="w-100 overflow-hidden">
    <div class="w-100 flex-center flex-column mt-5 mb-2" >
      <span class="text_title_swiper"  v-if="typeCmp === 'sec4'">جدیدترین محصولات</span>
      <span class="text_title_swiper"  v-if="typeCmp === 'sec6'">برخی از مشتریان ما</span>
      <div class="d-flex flex-column text-center text_description_swiper"  v-if="typeCmp === 'sec6'">
        <span>تامین منافع مشتری از جمله اهداف مهم در شرکت می‌مد می‌باشد </span>
        <span>و باعث افتخار ماست که توانسته‌ایم با کیفیت و توانایی‌های خود رضایت مشتریان خود را جلب کنیم.</span>
      </div>
      <div class="d-flex flex-row my-4">
        <div class="icon_R_L" @click="prev"><img src="../../assets/img/icon/right.svg" alt=""></div>
        <div class="icon_R_L" @click="next"><img src="../../assets/img/icon/left.svg" alt=""></div>
      </div>
    </div>
    <div class="swiper-container-card-sec4"  v-if="typeCmp === 'sec4'">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="(items , index) in itemsSwipe1"  >
          <cardItemsShop :dataCard="items"/>
        </div>
      </div>
    </div>
    <div class="swiper-container-card-sec6"  v-if="typeCmp === 'sec6'">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="(items , index) in itemsSwipe2"  >
          <div class="box_items_s2"><img :src="items.img" alt=""></div>
        </div>
      </div>
    </div>
   </div>
</template>
<style>
/************************************ Box ****************************************/
.swiper-container-card-sec4 , .swiper-container-card-sec6{
  overflow: hidden;
  position: relative;
}

.swiper-wrapper {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
}

.swiper-slide {
  width: auto!important;
  position: relative;
  margin: 0 12px 0 12px
}

.text_title_swiper{
  font-weight: 700;
  font-size: 20px;
  color: #000000;
}
.text_description_swiper{
  font-weight: 500;
  font-size: 14px;
  color: #88A6C5;
  margin-top: 10px;
}
.icon_R_L{
  padding: 10px;
  cursor: pointer;
  background: #FFFFFF;
  border-radius: 50%;
  margin: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}

/*s2*/

.box_items_s2 {
  min-height: 11rem;
  width: 11rem;
  background: #FFFFFF;
  box-shadow: 5px 10px 30px -15px rgba(0, 0, 0, 0.1);
  border-radius: 20px;
  gap: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.box_items_s2 img {
  max-width: 100%;
  padding: 20px;
  display: flex;
  height: 100%;

  filter: grayscale(1);
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
import Swiper from 'swiper'
import 'swiper/swiper-bundle.css'
import cardItemsShop from "../helperComponents/cardItemsShop.vue";
import img1 from "../../assets/img/icon/sec2/sec2iconitems1.svg"
import img2 from "../../assets/img/icon/sec2/sec2iconitems2.svg"
import img3 from "../../assets/img/icon/sec2/sec2iconitems3.svg"
import img4 from "../../assets/img/icon/sec2/sec2iconitems4.svg"
import img5 from "../../assets/img/icon/sec6/Emam-Khomeyni-Hospital-Logo 1.svg"
import img6 from "../../assets/img/icon/sec6/Khatam-Anbiya-Hospital-Kogo 1.svg"
import img7 from "../../assets/img/icon/sec6/logo-helal-ahmar 1.svg"
import img8 from "../../assets/img/icon/sec6/Mehr-Hospital-Logo 1.svg"
import img9 from "../../assets/img/icon/sec6/Pars-Hospital-Logo 1.svg"
import img10 from "../../assets/img/icon/sec6/logo-milad-tower 1.svg"

export default {
  props: {
    typeCmp:String,
    options1:{
      type: Object,
      default: () => ({
        breakpoints: {
          360: {
            slidesPerView: 1,
            spaceBetween: 0,
          },
          400: {
            slidesPerView: 1.11,
            spaceBetween: 0,
          },
          450: {
            slidesPerView: 1.26,
            spaceBetween: 0,
          },
          576: {
            slidesPerView: 1.53,
            spaceBetween: 0,
          },
          768: {
            slidesPerView: 2.07,
            spaceBetween: 0,
          },
          992: {
            slidesPerView: 2.77,
            spaceBetween: 0,
          },
          1200: {
            slidesPerView: 3.32,
            spaceBetween: 0,
          },
          1400: {
            slidesPerView: 3.78,
            spaceBetween: 0,
          },
        },
      }),
    },
    options2: {
      type: Object,
      default: () => ({
        breakpoints: {
          360: {
            slidesPerView: 1.67,
            spaceBetween: 0,
          },
          400: {
            slidesPerView: 1.87,
            spaceBetween: 0,
          },
          450: {
            slidesPerView: 2.14,
            spaceBetween: 0,
          },
          576: {
            slidesPerView: 2.6,
            spaceBetween: 0,
          },
          768: {
            slidesPerView: 3.51,
            spaceBetween: 0,
          },
          992: {
            slidesPerView: 4.7,
            spaceBetween: 0,
          },
          1200: {
            slidesPerView: 5.6,
            spaceBetween: 0,
          },
          1400: {
            slidesPerView: 6.5,
            spaceBetween: 0,
          },
        },
      
      })
    }
  },
  components:{
    cardItemsShop
  },
  data() {
    return {
      swiper1: null,
      swiper2: null,
      itemsSwipe1: [
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
      ],
      itemsSwipe2: [
        {
          img:img5,
          id:0
        },
        {
          img:img6,
          id:1
        },
        {
          img:img7,
          id:2
        },
        {
          img:img8,
          id:3
        },
        {
          img:img9,
          id:4
        },
        {
          img:img10,
          id:5
        },
        {
          img:img9,
          id:6
        },
      ]
    }
  },
  mounted() {
    this.initSwiper()
  },
  methods: {
    initSwiper() {
      this.swiper1 = new Swiper('.swiper-container-card-sec4', this.options1)
      this.swiper2 = new Swiper('.swiper-container-card-sec6', this.options2)
    },
    next(){
      console.log(this.typeCmp)
      if (this.typeCmp==="sec4"){
        this.swiper1.slidePrev()
      }else {
        this.swiper2.slidePrev()
      }
    },
    prev(){
      console.log(this.typeCmp)
      if (this.typeCmp==="sec4"){
        this.swiper1.slideNext()
      }else {
        this.swiper2.slideNext()
      }
    }
  }
}
</script>
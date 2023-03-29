<template>
    <div class="w-100 flex-center" >
    <div class="box_category flex-wrap" v-if="typeCmp==='sec_header'">
      <div class="w-100 overflow-hidden">
        <div class="swiper-container-header">
            <div class="swiper-wrapper">
              <div class="swiper-slide" v-for="items in data_swipe1" :key="items.key">
                <div class="items_category mt-2">
                  <div class="img_category">
                    <img :src="items.img" style="width: 100% ; height: 100% ; object-fit: cover" alt="">
                  </div>
                  <span>{{items.text}}</span>
              </div>
                </div>
            </div>
        </div>
      </div>
    </div>
    <div class="w-100 overflow-hidden" v-if="typeCmp==='sec_2_nav'">
          <div class="swiper-container-sec2-nav">
              <div class="swiper-wrapper d-flex justify-content-between">
                <div class="swiper-slide cursor_pointer" v-for="items in data_swipe2" :key="items.key"  @click="handleClick(items.category)">
                  <span class="mt-2">{{ items.text }}</span>
                </div>
              </div>
          </div>
    </div> 
      <div class="swiper-container-sec2-content w-100 overflow-hidden " v-if="typeCmp==='sec_2_content'">
        <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="(items , index) in data_swipe3"  >
            <cardItemsShop :dataCard="items"/>
          </div>
        </div>
      </div> 
  </div>
  </template>
  <style>
  /************************************ Box ****************************************/
  .swiper-container-header , .swiper-container-sec2-nav{
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
    width: 100%!important;
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
      SwiperhandleClick: Function,
      data_swipe1:[],
      data_swipe2:[],
      data_swipe3:[],
      options1: {
        type: Object,
        default: () => ({
          breakpoints: {
            350: {
              slidesPerView: 1.4,
              spaceBetween: 0,
            },
            400: {
              slidesPerView: 1.7,
              spaceBetween: 0,
            },
            450: {
              slidesPerView: 1.89,
              spaceBetween: 0,
            },
            576: {
              slidesPerView: 2.3,
              spaceBetween: 0,
            },
            768: {
              slidesPerView: 3,
              spaceBetween: 0,
            },
            992: {
              slidesPerView: 4.2,
              spaceBetween: 0,
                          },
            1200: {
              slidesPerView: 5,
              spaceBetween: 0,
              allowTouchMove: false,
            },
          }
        })
      },
      options2: {
        type: Object,
        default: () => ({
          breakpoints: {
            350: {
              slidesPerView: 2.2,
              spaceBetween: 0,
            },
            400: {
              slidesPerView: 2.7,
              spaceBetween: 0,
            },
            450: {
              slidesPerView: 3.1,
              spaceBetween: 0,
            },
            576: {
              slidesPerView: 4.1,
              spaceBetween: 0,
            },
            768: {
              slidesPerView: 5,
              spaceBetween: 0,
            },
            992: {
              slidesPerView: 5,
              spaceBetween: 0,
            },
            1200: {
              slidesPerView: 5,
              spaceBetween: 0,
            },
          }
        })
      },
      options3: {
      type: Object,
      default: () => ({
        breakpoints: {
          360: {
            slidesPerView: 1,
            spaceBetween: 0,
          },
          400: {
            slidesPerView: 1.12,
            spaceBetween: 0,
          },
          450: {
            slidesPerView: 1.26,
            spaceBetween: 0,
          },
          576: {
            slidesPerView: 1.52,
            spaceBetween: 0,
          },
          768: {
            slidesPerView: 2.05,
            spaceBetween: 0,
          },
          992: {
            slidesPerView: 2.7,
            spaceBetween: 0,
          },
          1200: {
            slidesPerView: 3.3,
            spaceBetween: 0,
          },
          1400: {
            slidesPerView: 3.8,
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
        swiper3: null,
        itemsSwipe: [
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
        this.swiper1 = new Swiper('.swiper-container-header', this.options1)
        this.swiper2 = new Swiper('.swiper-container-sec2-nav', this.options2)
        this.swiper3 = new Swiper('.swiper-container-sec2-content', this.options3)
      },
      handleClick(data) {
      this.SwiperhandleClick(data);
      // console.log(data)
      }
      
    }
  }
  </script>
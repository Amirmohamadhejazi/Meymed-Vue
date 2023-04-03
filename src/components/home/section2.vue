<template>
  <div class="box_menu_sec2">
    <div class="menu_inner_t col-12 col-lg-11 flex-wrap">
      <swiper typeCmp="sec_2_nav" :data_swipe2="itemsNav" :SwiperhandleClick="handleClickSwiper" :currentCategory="currentCategory"/>
    </div>
    <div class="menu_inner_b col-11 col-lg-10"/>
  </div>
  <div class="w-100 flex-center">
    <div :class="`w-100 d-flex ${filteredItems.length <= 2 ? 'justify-content-start' : 'justify-content-center'} align-items-center flex-wrap  sec2-content-des ` " v-if="width_desc" >
      <cardItemsShop v-for="items in filteredItems" :dataCard="items"/> 
    </div> 
    <swiper typeCmp="sec_2_content" :data_swipe3="filteredItems" v-else/>
  </div>
</template>

<style>
/************************************ Box ****************************************/
.box_menu_sec2{
  position: relative;
  margin-top: 80px;
  background: transparent;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: start;
  font-size: 12px;
  margin-bottom: 120px; 
}
.menu_inner_t ,.menu_inner_b{
  position: absolute;
  border-radius: 20px;
  box-shadow: 5px 10px 30px -15px rgba(0, 0, 0, 0.1);
}
.menu_inner_t{
  /* padding: 30px; */
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-weight: 700;
font-size: 14px;
color: #616161;
  height: 103px;
  background: #FFFFFF;
  z-index: 1;
}
.menu_inner_b{
  height: 113px;
  background: #B4D9FF;
}
.items_sec_2_nav{
  border-radius: 10px;
  padding: 15px;
}
.items_sec_2_nav_Active{
  font-weight: 700;
font-size: 14px;
color:black;
    background-color: #F4FAFF;
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
import cardItemsShop from "../helperComponents/cardItemsShop.vue";
import img1 from "../../assets/img/icon/sec2/sec2iconitems1.svg"
import img2 from "../../assets/img/icon/sec2/sec2iconitems2.svg"
import img3 from "../../assets/img/icon/sec2/sec2iconitems3.svg"
import img4 from "../../assets/img/icon/sec2/sec2iconitems4.svg"
import img5 from "../../assets/img/icon/sec2/sec2iconitems5.svg"
import img6 from "../../assets/img/icon/sec2/sec2iconitems6.svg"
import img7 from "../../assets/img/icon/sec2/sec2iconitems7.svg"
import img8 from "../../assets/img/icon/sec2/sec2iconitems8.svg"
import img9 from "../../assets/img/icon/formdoctor.png"
import img10 from "../../assets/img/icon/SurgicalBlade.png"
import img11 from "../../assets/img/icon/hospitalbed.jpg"
import img12 from "../../assets/img/icon/hospitalbed2.jpg"
import img13 from "../../assets/img/icon/hospitalbed3.jpg"
import img14 from "../../assets/img/icon/hospitalbed4.jpg"
import img15 from "../../assets/img/icon/Medicalinstruments.png"
import swiper from "@/components/helperComponents/swiper.vue";

export default {
  data() {
    return {
      number_option: 0,
      swiper1: null,
      width_desc :undefined ,
      itemsNav:[
        {text:"دستگاه های پزشکی ",
          category:"category1",
        id:0},
        {text:"تجهیزات اتاق عمل",
          category:"category2",
        id:1},
        {text:"روپوش‌های پزشکی",
          category:"category3",
        id:2},
        {text:"تخت‌های بیمارستانی",
          category:"category4",
        id:3},
        {text:"ابزار پزشکی",
          category:"category5",
        id:4},
      ],
      itemsCard: [
        {
          img:img4,
          title:"کد 84514",
          description:"تب سنج دیجیتال رز دیتا",
          price:45000,
          percentage:0,
          category: 'category5'
        },
        {
          img:img3,
          title:"کد 81544",
          description:"تب سنج دیجیتال رز دیتا",
          price:68479,
          percentage:0,
          category: 'category5'
        },
        {
          img:img2,
          title:"کد 823014",
          description:"تب سنج دیجیتال رز دیتا",
          price:547920,
          percentage:10,
          category: 'category5'
        },
        {
          img:img1,
          title:"کد 81774",
          description:"تب سنج دیجیتال رز دیتا",
          price:390000,
          percentage:6,
          category: 'category5'
        },
        {
          img:img8,
          title:"کد 81055",
          description:"تب سنج دیجیتال رز دیتا",
          price:390000,
          percentage:45,
          category: 'category5'
        },
        {
          img:img7,
          title:"کد 81114",
          description:"تب سنج دیجیتال رز دیتا",
          price:1221120,
          percentage:23,
          category: 'category5'
        },
        {
          img:img6,
          title:"کد 83014",
          description:"تب سنج دیجیتال رز دیتا",
          price:504873,
          percentage:12,
          category: 'category5'
        },
        {
          img:img5,
          title:"کد 81114",
          description:"تب سنج دیجیتال رز دیتا",
          price:10002000,
          percentage:65,
          category: 'category5'
        },
        {
          img:img12,
          title:"کد 12111",
          description:"تخت بیمارستانی",
          price:102000,
          percentage:65,
          category: 'category4'
        },
        {
          img:img13,
          title:"کد 1321",
          description:"تخت بیمارستانی",
          price:1020540,
          percentage:65,
          category: 'category4'
        },
        {
          img:img9,
          title:"کد 1212",
          description:"روپوش پزشکی",
          price:10002000,
          percentage:65,
          category: 'category3'
        },
        {
          img:img10,
          title:"کد 1231",
          description:"تیغ جراحی",
          price:10002000,
          percentage:65,
          category: 'category2'
        },
        {
          img:img1,
          title:"کد 1231",
          description:"تخت بیمارستانی",
          price:10002000,
          percentage:65,
          category: 'category4'
        },
        {
          img:img14,
          title:"کد 1231",
          description:"تخت بیمارستانی",
          price:10002000,
          percentage:65,
          category: 'category4'
        },
        {
          img:img15,
          title:"کد 1231",
          description:"مانیتورینگ",
          price:1502000,
          percentage:65,
          category: 'category1'
        },

      ],
      currentCategory: 'category1'
    }
  },
  components:{
    cardItemsShop,
    swiper
  },
  mounted() {
    setInterval(()=>{
      // console.log(this.width_desc);
      return this.width_desc = window.innerWidth > 1200
    },[1000])
  },
  computed: {
    filteredItems() {
      let filteredItems = this.itemsCard
      if (this.currentCategory !== 'all') {
        filteredItems = filteredItems.filter(item => item.category === this.currentCategory)
      }
      return filteredItems
    },
  },
  methods: {
    filter(category) {
      this.currentCategory = category
    },
    initSwiper() {
      this.swiper = new Swiper('.swiper-container1', this.options)
    },
    handleClickSwiper(data) {
      this.filter(`${data}`)

      // console.log(data)
    },
  }
}
</script>
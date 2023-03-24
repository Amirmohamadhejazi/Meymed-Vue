<template>
  <div class="box_menu_sec2">
    <div class="menu_inner_t col-12 col-lg-11 flex-wrap">
      <span class="mt-2">دستگاه‌های پزشکی</span>
      <span class="mt-2">تجهیزات اتاق عمل</span>
      <span class="mt-2">روپوش‌های پزشکی</span>
      <span class="mt-2">تخت‌های بیمارستانی</span>
      <span class="mt-2">ابزار پزشکی</span>
    </div>
    <div class="menu_inner_b col-11 col-lg-10"/>
  </div>
  <div class="w-100 d-flex justify-content-between flex-wrap">
    <cardItemsShop v-for="items in itemsCard" :dataCard="items"/>
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
  padding: 30px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: black;
  height: 103px;
  background: #FFFFFF;
  z-index: 1;
}
.menu_inner_b{
  height: 113px;
  background: #B4D9FF;
}

/************************************ search form ****************************************/


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
export default {
  data() {
    return {
      number_option: 0,
      itemsCard: [
        {
          img:img4,
          title:"کد 84514",
          description:"تب سنج دیجیتال رز دیتا",
          price:45000,
          percentage:0
        },
        {
          img:img3,
          title:"کد 81544",
          description:"تب سنج دیجیتال رز دیتا",
          price:68479,
          percentage:0
        },
        {
          img:img2,
          title:"کد 823014",
          description:"تب سنج دیجیتال رز دیتا",
          price:547920,
          percentage:10
        },
        {
          img:img1,
          title:"کد 81774",
          description:"تب سنج دیجیتال رز دیتا",
          price:390000,
          percentage:6
        },
        {
          img:img8,
          title:"کد 81055",
          description:"تب سنج دیجیتال رز دیتا",
          price:390000,
          percentage:45
        },
        {
          img:img7,
          title:"کد 81114",
          description:"تب سنج دیجیتال رز دیتا",
          price:1221120,
          percentage:23
        },
        {
          img:img6,
          title:"کد 83014",
          description:"تب سنج دیجیتال رز دیتا",
          price:504873,
          percentage:12
        },
        {
          img:img5,
          title:"کد 81114",
          description:"تب سنج دیجیتال رز دیتا",
          price:10002000,
          percentage:65
        },

      ]
    }
  },
  components:{
    cardItemsShop
  },
  methods:{
    changeTab(data) {
      this.number_option = data
    },
    handleSubmit() {
      this.$emit('submit', this.form)
      console.log(this.form)
    }

  }
}
</script>

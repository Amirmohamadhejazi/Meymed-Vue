<template>
   <div class="box_content_sec5  d-flex flex-lg-row justify-content-lg-between flex-column  my-lg-5 ">
    <div class="col-12 col-lg-6 m-2  box_items1 align-items-center text-center justify-content-lg-between" >
      <span class="text-title-sec5">پیشنهاد ویژه</span>
      <span class=" text-desc-sec5">انواع تجهیزات پزشکی مخصوص اتاق عمل از معتبرترین برندهای موجود در بازار با تخفیف اختصاصی ویژه فروشگاه می‌مد به مدت محدود</span>
      <div class="w-100 d-flex flex-column flex-lg-row justify-lg-content-between align-items-lg-end ">
        <div class="d-flex col-12 col-lg-6 flex-row justify-content-between">
          <div class="d-flex flex-column">
            <span class="title_detail">ثانیه</span>
            <span class="value_detail">{{timeCount.s}}</span>
          </div>
          <div class="d-flex flex-column">
            <span class="title_detail">دقیقه</span>
            <span class="value_detail">{{timeCount.m}}</span>
          </div>
          <div class="d-flex flex-column">
            <span class="title_detail">ساعت</span>
            <span class="value_detail">{{timeCount.h}}</span>
          </div>
          <div class="d-flex flex-column">

            <span class="title_detail">روز</span>
            <span class="value_detail">{{timeCount.d}}</span>
          </div>
        </div>
        <div class="d-flex justify-content-center justify-content-lg-end col-12 col-lg-6 ">
          <div class="btn_box_items">
            <span>مشاهده بیشتر</span>
          </div>
        </div>
      </div>
    </div>
    <div class="col-12 col-lg-6 d-flex m-2 align-items-start justify-content-center justify-content-lg-between box_items2"  >
       <div class="w-100 d-flex flex-column-reverse flex-lg-row text-center justify-content-lg-between align-items-center align-items-lg-start">
        <div class="d-flex flex-column text-title-sec5 mt-3 mt-lg-0">
          <span>بیش از 30 درصد تخفیف</span>
          <span> برای محصولات برند رزمکس</span>
        </div>
        <div><img src="../../assets/img/icon/sec5Logo.svg" alt=""></div>
      </div>
      <div class="w-100 d-flex flex-column text-desc-sec5 my-lg-3 align-items-center align-items-lg-start  my-3 my-lg-0">
        <span>محصولات نمونه برند رزمکس</span>
        <span> با تکنولوژی برتر و بالاترین کیفیت</span>
      </div>
        <div class="d-flex justify-content-center justify-content-lg-start align-items-start col-12 col-lg-12  ">
          <div class="btn_box_items">
            <span>مشاهده بیشتر</span>
          </div>
        </div>
    </div>
    </div>
 </template>

<script>
export default {

  components:{},
  data() {
    return {
      timeCount :{d:"" ,h:"" ,m:"" ,s:"" }
    }
  },
  methods: {
    getTime(){
      let countDownDate = new Date("April 1, 2023 15:37:25").getTime();
      setInterval(()=> {
        let now = new Date().getTime();
        let distance = countDownDate - now;
        let days = Math.floor(distance / (1000 * 60 * 60 * 24));
        let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        let seconds = Math.floor((distance % (1000 * 60)) / 1000);
        this.timeCount = {d:days ,h:hours ,m:minutes ,s:seconds }
      }, 1000);
    },
  },
  mounted() {
    this.getTime();
  }
}
</script>

<style>
.box_content_sec5{
  width: 100%;
  margin-top: 50px;
}
.box_items1 , .box_items2{
  display: flex;
  flex-direction: column;
  border-radius: 10px;
  height: 20rem;
  padding: 30px;
  justify-content: center;
}
.box_items1{
  background: url('/src/assets/img/icon/sec5icon2.svg'), #9FC1E5;
  background-repeat: no-repeat;
  background-position:right;
}
.box_items2{
  background: url('/src/assets/img/icon/sec5icon1.svg'), #FFFFFF;
  background-repeat: no-repeat;
  background-position:left bottom;
}


.btn_box_items{
  border-radius: 10px;
  padding: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

.box_items1 .btn_box_items{
  background: #FFFFFF;
  color: #84A6CA;
}
.box_items2 .btn_box_items{
  background: #4A95E3;
  color: #FFFFFF;
}


.box_items1 .text-title-sec5{
  font-weight: 800;
  font-size: 36px;
  color: #FFFFFF;
}
.box_items2 .text-title-sec5{
  font-weight: 700;
  font-size: 24px;
  text-align: right;
  color: #000000;
}


.box_items1 .text-desc-sec5{
  font-weight: 700;
  font-size: 16px;
  color: #FFFFFF;
  width: 90%;
}
.box_items2 .text-desc-sec5{
  font-weight: 400;
  font-size: 16px;
  text-align: right;
  color: #000000;
}

.title_detail{
  font-weight: 500;
  font-size: 13px;
  text-align: center;
  color: #FFFFFF;
}

.value_detail{
  font-weight: 800;
  font-size: 36px;
  text-align: center;
  color: #FFFFFF;
}

</style>

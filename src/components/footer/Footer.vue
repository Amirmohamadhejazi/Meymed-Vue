<template>
  <div class="box_footer">

    <div class="box_top_footer1"></div>
    <div class="box_top_footer2"></div>

  </div>
  <span class="text_end_footer">  استفاده از مطالب فروشگاه اینترنتی می مد فقط برای مقاصد غیرتجاری و با ذکر منبع بلامانع است. کلیه حقوق این سایت متعلق به شرکت لوازم پزشکی میثم طبرستان (فروشگاه اینترنتی تجهیزات پزشکی و بیمارستانی می مد) می‌باشد.</span>
</template>

<script>
export default {

  components:{
  },
  data() {
    return {
    }
  },


}
</script>

<style>
.box_footer{
  position: relative;
  width: 100%;
  margin-top: 150px;
  height: 900px;
  background: #4484C6;
  border-radius: 100px;
}


.box_top_footer1{
  position: absolute;
  width: 75%;
  height: 312px;
  background: #FFFFFF;
  border-radius: 50px;
   box-shadow: 5px 10px 30px -15px rgba(0, 0, 0, 0.1);
  top: 0;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
}
.box_top_footer2{
  position: absolute;
  width: 60%;
  height: 312px;
  background: #609CDB;
  border-radius: 50px;
  top: 3%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 1;
}
.text_end_footer{
  width: 80%;
  text-align: center;
  font-weight: 400;
  font-size: 12px;
  color: #A2B8CA;
}
</style>

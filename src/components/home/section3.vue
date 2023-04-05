<template>
  <div class="content_box_sec3 d-flex flex-lg-row justify-content-lg-between align-items-center  flex-column ">
    <div class="box1 d-flex flex-lg-row align-items-center flex-column-reverse ">
      <div class="col-lg-6 col-12 d-flealign-items-centerx align-items-lg-start align-items-center flex-column pe-3  ">
        <span>انواع محصولات ضدعفونی کننده</span>
        <div class="box_btn  mt-3 mb-3 mb-lg-0">مشاهده بیشتر</div>
      </div>
      <div class="col-lg-6 col-12 flex-center ">
        <div class="p5 mt-3 mt-lg-0">
          <img src="../../assets/img/icon/sec3icon_shampo.svg" style="width: 100% ; height: 100% ; object-fit: cover"  alt="">
        </div>
      </div>
    </div>
    <div class="box2  d-flex flex-lg-row align-items-center flex-column-reverse ">
      <div class="col-lg-6 col-12 d-flex align-items-lg-start align-items-center flex-column pe-3 ">
        <span>ماسک‌های N95 مدل سه‌بعدی</span>
        <div class="box_btn  mt-3 mb-3 mb-lg-0 ">مشاهده بیشتر</div>
      </div>
      <div class="col-lg-6 col-12 flex-center ">
        <div class="p5 mt-3 mt-lg-0">
          <img src="../../assets/img/icon/sec3icon_mask.svg" style="width: 100% ; height: 100% ; object-fit: cover"  alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<style>
/************************************ Box ****************************************/
.content_box_sec3{
  margin-top: 100px;
  width: 100%;
  color: black;
  font-size: 28px;
}
.box1, .box2{
  min-height: 320px;
  border-radius: 30px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 10px;
  width: 100%;
}
.box1{

  background: url('/src/assets/img/icon/sec3bg2.svg'), #C1E0FF;
  background-repeat: no-repeat;
  background-position:left 0 ;
}
.box2{

  background: url('/src/assets/img/icon/sec3bg1.svg'), rgba(247, 199, 55, 0.4);
  background-repeat: no-repeat;
  background-position:left 32px ;
}
.box_btn{
  width: 140px;
  height: 55px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 7px;
  font-size: 16px;
  font-weight: 600;
}
.box2 .box_btn {
  background: #F7C737;

}
.box1 .box_btn {
  background: #4A95E3;
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


export default {
  data() {
    return {
      number_option: 0,
    }
  },
  components:{
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

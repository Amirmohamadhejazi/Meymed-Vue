<template>
  <div class="content_box flex-column flex-lg-row">
    <div class="item_box col-12 col-lg-7 ">
      <div class="d-flex flex-row justify-content-between flex-wrap">
        <div :class="[items.id  === number_option ? 'options_box_select options_box_selected' : 'options_box_select' ]" v-for="items in items_options" :key="items.id" @click="changeTab(items.id)">
          <img :src="items.img" alt="">
          <span class="mt-3">{{items.text}}</span>
        </div>
      </div>
      <div class="d-flex flex-column my-3">
        <span>لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است</span>
        <span>لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است</span>
        <span>لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است</span>
      </div>

        <form class="d-flex flex-row justify-content-between flex-wrap" @submit.prevent="handleSubmit">

          <div class="input-group flex-nowrap boxes_under_options">
            <input type="text" class="form-control inputCustom" placeholder="نام و نام خانوادگی" aria-label="name" aria-describedby="addon-wrapping" name="name" v-model="form.name">
          </div>
          <div class="input-group flex-nowrap boxes_under_options">
            <input type="text" class="form-control inputCustom" placeholder="شماره تماس" aria-label="phone" aria-describedby="addon-wrapping" name="phone"  v-model="form.phone">
          </div>
          <div class="input-group flex-nowrap boxes_under_options">
            <input type="text" class="form-control inputCustom" placeholder="استان" aria-label="ost" aria-describedby="addon-wrapping" name="ost"  v-model="form.ost">
          </div>
          <div class="input-group flex-nowrap boxes_under_options">
            <input type="text" class="form-control inputCustom" placeholder="شهر" aria-label="city" aria-describedby="addon-wrapping" name="city" v-model="form.city" >
          </div>
          <div class="input-group flex-nowrap boxes_under_options">
            <input type="text" class="form-control inputCustom" placeholder="توضیحات محصول" aria-label="detail" aria-describedby="addon-wrapping" name="detail" v-model="form.detail" >
          </div>
          <div class="boxes_under_options bg_yellow">
            <button type="submit"  >ثبت درخواست</button>

          </div>
        </form>


    </div>
    <div class="item_box d-flex align-content-center justify-content-end text-center flex-column col-12 col-lg-4 gap10">
      <div class="img_detail_selected">
        <img src="../../assets/img/icon/emojione_hospital.svg" alt="">
      </div>
      <span class="font_lg mt-5" >{{items_options[number_option].text}}</span>
      <div class="w-100 d-flex justify-content-center font_sm">
        <span class="mt-3 w-75">لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است، چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است، و برای شرایط فعلی تکنولوژی مورد نیاز، و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد، کتابهای زیادی در شصت و سه درصد گذشته حال و آینده، شناخت فراوان جامعه و متخصصان را می طلبد</span>
      </div>
    </div>
  </div>
</template>

<style>
/************************************ Box ****************************************/
.content_box{
  display: flex;
  justify-content: space-between;
}
.item_box{
  color: #000000;
  margin-top: 100px;
  position: relative;
  padding: 30px;
  background: #FFFFFF;
  box-shadow: 5px 10px 30px -15px rgba(0, 0, 0, 0.1);
  border-radius: 20px;
}

/*1*/
.img_detail_selected {
  position: absolute;
  width: 145px;
  height: 145px;
  border-radius: 50%;
  top: 0;
  left: 50%;
  transform: translate(-50%, -50%);
  background: linear-gradient(180deg, #E1ECF4 0%, rgba(244, 250, 255, 0) 100%);
  display: flex;
  justify-content: center;
  align-items: center;
}

/*2*/
.options_box_select{
  cursor: pointer;
  font-size: 12px;
  width: 95px;
  height: 95px;
  background: #FFFFFF;
  color: #A5A5A5;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.options_box_selected{
  background: #ebebeb;
  color: #4A95E3;
}

.boxes_under_options{
  width: 30%;
  height: 60px;
  background: #e8e8e8;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 10px;
  border-radius: 15px;
  font-size: 14px;
}
.boxes_under_options input{
  height: 100%;
  font-size: 14px;
}

.boxes_under_options button{
  border: 0;
  width: 100%;
  height: 100%;
  background: transparent;

}

.bg_yellow{
  background: #F7C737;

}
.font_lg{
  font-size: 18px ;
  font-weight: 700
}
.font_sm{
  font-size: 12px ;
  font-weight: 400
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

export default {
  data() {
    return {
      number_option: 0,
      form: {
        name: '',
        phone: '',
        ost: '',
        city: '',
        detail: ''
      },
      items_options:[
        {
          text:"سازمانی",
          img:"../src/assets/img/icon/sec1_icon5.svg",
          id:4
        },
        {
          text:"استعلام قیمت",
          img:"../src/assets/img/icon/sec1_icon4.svg",
          id:3
        },
        {
          text:"درخواست دمو",
          img:"../src/assets/img/icon/sec1_icon3.svg",
          id:2
        },
        {
          text:"درخواست خدمات",
          img:"../src/assets/img/icon/sec1_icon2.svg",
          id:1
        },
        {
          text:"درخواست تعمیرات",
          img:"../src/assets/img/icon/sec1_icon1.svg",
          id:0
        }
      ]
    }
  },
  components:{
  },
  methods:{
    changeTab(data) {
      this.number_option = data
    },
    // formSubmit(values, {resetForm}) {
    //   console.log(values)
    //   // console.log(resetForm)
    // },

    handleSubmit() {
      this.$emit('submit', this.form)
      console.log(this.form)
    }

  }
}
</script>

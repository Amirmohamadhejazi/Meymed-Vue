<template>
<!--  <h1>{{// dataCard.id}}</h1>-->
     <div class="box_items">
      <div class="d-flex flex-center">
        <img :src="dataCard.img"  class="img-cover"   alt="">
      </div>
      <span class="title">{{dataCard.title}}</span>
      <span class="description">{{dataCard.description}}</span>
      <div class="d-flex justify-content-between align-items-center mt-3">
        <img src="../../assets/img/icon/heart.svg" alt="">
        <div class="d-flex flex-column align-items-end" v-if="dataCard.price">
          <div class="d-flex flex-row">
            <span class="badge_percentage" v-if="dataCard.percentage">{{dataCard.percentage}}%</span>
            <span class="text_old_price mx-1"  v-if="dataCard.percentage">{{separateNumber(dataCard.price)}}</span>
            <span>تومان</span>
          </div>
          <span class="text_price">{{dataCard.percentage? separateNumber(Math.round(dataCard.price - dataCard.price/100*dataCard.percentage))  :separateNumber(dataCard.price)}}</span>
        </div>
        <span class="call_price" v-if="!dataCard.price">استعلام قیمت با ثبت درخواست</span>
      </div>
    </div>
</template>

<style>
.box_items{
  margin-top: 20px;
  position: relative;
  padding: 30px;
  background: #FFFFFF;
  box-shadow: 5px 10px 30px -15px rgba(0, 0, 0, 0.1);
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  justify-content: end;
  font-size: 14px;
  color: black;
  margin: 10px; 
}
.box_items .title{
  color: #3C3C3C;
  font-size: 12px;
}
.box_items .description{
  color: #A3A3A3;
  font-size: 12px;
}
.box_items .call_price{
  color: #3C3C3C;
  font-size: 14px;
}

.text_old_price{
  color: #C5C5C5;
  text-decoration: line-through #C5C5C5;
}
.text_price{
  font-size: 20px;
}
.badge_percentage{
  padding: 0 8px 0 8px;
  color: white;
  background: #FF4A4A;
  border-radius: 7px;
}
.img-cover{
  width: 100%;
    aspect-ratio: 3/2;
    object-fit: contain;
    height: 156px;
    width: 208;
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
  props: {
    dataCard: {},
    myProp:{}
  },
  data() {
    return {
      number_option: 0
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
    },
    separateNumber( num ) {
      let str = num.toString().split('.');
      if (str[0].length >= 5) {
        str[0] = str[0].replace(/(\d)(?=(\d{3})+$)/g, '$1,');
      }
      if (str[1] && str[1].length >= 5) {
        str[1] = str[1].replace(/(\d{3})/g, '$1 ');
      }
      return str.join('.');
    }

  }
}
</script>

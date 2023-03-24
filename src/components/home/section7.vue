<template>
  <span class="w-100 flex-center text_top">سوالات متداول</span>
  <div class="box_content  d-flex flex-lg-row justify-content-lg-between flex-column   ">
    <div class="col-12 col-lg-7  mt-2 p-2" >
      <collapse :items_collapse="items_clp"/>
    </div>
    <div class="col-12 col-lg-4 d-flex mt-2 p-2 align-items-start justify-content-center" >
      <img src="../../assets/img/icon/iconsec7.svg" alt="s"/>
    </div>
  </div>
</template>

<script>
import collapse from "@/components/helperComponents/collapse.vue";

export default {
  components:{
    collapse
  },
  data() {
    return {
      items_clp:[
        {
          title:"نحوه فعالیت فروشگاه اینترنتی تجهیزات پزشکی می مد به چه صورت است؟" ,
          desc:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid aspernatur consequatur explicabo facere neque obcaecati optio porro, qui ratione vitae? Cumque dolor doloremque dolorum excepturi expedita modi odit, quidem velit?"
        },
        {
          title:"کالای مورد نظرتان را در ساید می مد چگونه جستجو کنید؟" ,
          desc:"کالا ها و تجهیزات پزشکی موجود در سایت، همگی در بخش هایی مجزا دسته بندی شده اند و شما می توانید با ورود به هر دسته، از تنوع کالاهای موجود در آن دیدن کنید. همچنین در قسمت جستجوی سایت نیز می توانید نام برند یا محصول مورد نظرتان را درج و سپس گزینه های موجود در سایت را مشاهده نمایید."
        },
        {
          title:"روش های استعلام قیمت هر کالا چگونه است؟" ,
          desc:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid aspernatur consequatur explicabo facere neque obcaecati optio porro, qui ratione vitae? Cumque dolor doloremque dolorum excepturi expedita modi odit, quidem velit?"
        },
        {
          title:"نحوه پرداخت خرید هر کالا چگونه است؟" ,
          desc:"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid aspernatur consequatur explicabo facere neque obcaecati optio porro, qui ratione vitae? Cumque dolor doloremque dolorum excepturi expedita modi odit, quidem velit?"
        }
      ]
    }
  },
}
</script>
<style>
.box_content{
  width: 100%;
  margin-top: 50px;
}
.text_top{
  font-weight: 700;
  font-size: 20px;
  margin-top: 50px;
  color: #000000;
}
</style>

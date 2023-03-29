<template>
    <div class="w-100 mt-5 ">
        <div class="d-flex flex-column">
            <div class="d-flex justify-content-center align-items-center flex-wrap">
                <img src="../../assets/img/icon/sec7_icon_top.svg" alt="">
                <span class="text_top_sec7 mt-3 mt-lg-0">فروشگاه اینترنتی تجهیزات پزشکی، بیمارستانی و آزمایشگاهی می مد</span>
            </div>
            <div class="box_content_sec7 d-flex flex-column flex-lg-row align-items-center text-center justify-content-lg-between ">
                    <div class="col-12 col-lg-3 d-flex  justify-content-between justify-content-lg-center align-items-center mt-3 mt-lg-0"
                :class=" items.id!== 3 && 'border_left_box_content_items' "
                v-for="items in items_sec7">
                <span class="ms-lg-2">{{ items.text }}</span>
                <img :src="items.img" alt="">
                </div>
            </div>
            
        </div>
    </div>
</template>
  
<script> 
import img1 from "../../assets/img/icon/sec7icon1.svg"
import img2 from "../../assets/img/icon/sec7icon2.svg"
import img3 from "../../assets/img/icon/sec7icon3.svg"
import img4 from "../../assets/img/icon/sec7icon4.svg"
export default {
    components:{},
    data() {
        return {
            items_sec7 : [
                {
                    text:"پشتیبانی 24 ساعته",
                    img:img1,
                    id:0
                },
                {
                    text:"قیمت‌های به‌روز و رقابتی",
                    img:img2,
                    id:1
                },
                {
                    text:"ضمانت اصالت محصولات",
                    img:img3,
                    id:2
                },
                {
                    text:"ارسال با پست پیشتاز",
                    img:img4,
                    id:3
                },
            ]
        }
    },
}
</script>
<style>
.box_content_sec7{
    margin-top: 20px;
    width: 100%;
    padding: 20px;
    background: #73B1F2;
    border-radius: 15px;
    color: white;
}
.text_top_sec7{
    font-weight: 700;
    font-size: 18px;
    color: #000000;
}

.border_left_box_content_items{
    border-left: 1px #98C6F5 solid;
}

@media only screen and (max-width: 993px) {
    .border_left_box_content_items{
    border:0
}
}
</style>
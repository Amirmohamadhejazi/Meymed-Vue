
<template>
    <div class="navbar">
      <div class=" iconLogo" style="z-index: 4"><img src="src/assets/logo.svg"  width="100%" height="100%"  alt="icon"></div>
      <div class="input-group flex-nowrap position-relative input_search input_desktop">
        <div class="position-absolute iconInput" style="z-index: 6"><img src="src/assets/searchIcon.svg"  width="100%" height="100%"  alt="icon"></div>
        <input type="text" class="form-control inputCustom" placeholder="نام محصول یا برند مورد نظرتان را وارد نمایید!" aria-label="numberpeopel" aria-describedby="addon-wrapping" name="numberpeopel" >
      </div>
      <!-- <div class="inputNav flex-center bg-white" >
        <span class="familly_iranyekan_bold display_span_sell">سبد درخواست</span>
        <div class=" iconbtn" style="z-index: 4"><img src="src/assets/shopIcon.svg"  width="100%" height="100%"  alt="icon"></div>
      </div> -->
      <div class="d-flex flex-row flex-wrap">
        <div class="inputNav flex-center bg-white " >
          <span class="familly_iranyekan_bold display_span_sell">سبد درخواست</span>
          <div class=" iconbtn" style="z-index: 4"><img src="src/assets/shopIcon.svg"  width="100%" height="100%"  alt="icon"></div>
        </div>
        <div class="btn_menu_mob bg-white me-3"> 
          <div class="w-100 h-100 flex-center">
            <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasTop" aria-controls="offcanvasTop"  aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
          </div>
        </div>
      </div>
      

      <div class="inputNav flex-center bg_Saffron display_btn_nav_desc cursor_pointer">
        <div class="w-100 d-flex justify-content-around align-items-center">
          <div class="d-flex flex-column text-left">
            <span>۰۲۱</span>
            <span class="familly_iranyekan_bold">۹۱۱۰۱۴۹۱۹</span>
          </div>
          <div class=" iconbtn" style="z-index: 4"><img src="src/assets/callIcon.svg"  width="100%" height="100%"  alt="icon"></div>
        </div>
      </div>
      <div class="inputNav flex-center bg_TuftsBlue display_btn_nav_desc cursor_pointer">
        <div class="w-100 d-flex justify-content-around align-items-center text-center text-white">
          ورود | ثبت نام
        </div>
      </div>
 
    </div>
    <div class="input-group flex-nowrap position-relative input_search input_mob mb-lg-5">
      <div class="position-absolute iconInput" style="z-index: 4"><img src="src/assets/searchIcon.svg"  width="100%" height="100%"  alt="icon"></div>
      <input type="text" class="form-control inputCustom" placeholder="نام محصول یا برند مورد نظرتان را وارد نمایید!" aria-label="numberpeopel" aria-describedby="addon-wrapping" name="numberpeopel" >
    </div> 
    <nav class="navbar navbar-expand-xl bg-white rounded nav-canvas   nav_mobile_items "> 
      
      
        <div class="w-100 p-0 ">
        <button class="navbar-toggler menu_btn_mob" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasTop" aria-controls="offcanvasTop"  aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="offcanvas offcanvas-top" tabindex="-1" id="offcanvasTop" aria-labelledby="offcanvasTopLabel">
          <div class="offcanvas-header">
            <h5 class="offcanvas-title" id="offcanvasWithBackdropLabel"></h5>
            <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
          </div>
          <div class="offcanvas-body">
            <div class="d-flex  align-items-center justify-content-around">
              <div class="inputNav flex-center bg_TuftsBlue display_btn_nav_mobile cursor_pointer">
                <div class="w-100 d-flex justify-content-around align-items-center text-center text-white">
                  ورود | ثبت نام
                </div>
              </div> 
              <div class="inputNav flex-center bg_Saffron display_btn_nav_mobile mt-2 cursor_pointer">
                <div class="w-100 d-flex justify-content-around align-items-center">
                  <div class="d-flex flex-column text-left">
                    <span>۰۲۱</span>
                    <span class="familly_iranyekan_bold">۹۱۱۰۱۴۹۱۹</span>
                  </div>
                  <div class=" iconbtn" style="z-index: 4"><img src="src/assets/callIcon.svg"  width="100%" height="100%"  alt="icon"></div>
                </div>
              </div>
            </div>           
            <ul className="w-100 d-lg-flex justify-content-between navbar-nav p-0">
              <li className="nav-item" v-for="items in dataMenu">
                <a className="nav-link box_menu_items" aria-current="page" href="#">{{items.text}}</a>
               </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  <swiper typeCmp="sec_header" :data_swipe1="dataCategory"/>
</template>

<style>
/* ******************************************** align width */
.iconInput{
  width: 18px;
  top: 50%;
  left: 25px;
  transform: translate(-50%, -50%);
}
.iconLogo{
  /*width: 150px;*/
}
.iconbtn{
  width: 18px;
}

.input_search {
  max-width: 45%;
}

/* ******************************************** Navbar */

.display_btn_nav_mobile{
    display: none!important;
  }

/************************************ Box ****************************************/

.input_mob{
  display: none;
}
.input_desktop{
  display: flex;
}


.navbar{
  width: 100%;
  gap: 10px;
}
.inputNav{
  height: 55px;
  border-radius: 15px;
  font-size: 14px;
  max-width: 160px;
  padding: 16px;
}

.box_menu{
  width: 100%;
  background: #FFFFFF;
  box-shadow: 5px 8px 30px -15px rgba(0, 0, 0, 0.1);
  border-radius: 15px;
  display: flex;
  justify-content: space-between;
  padding: 20px;
}
.box_menu_items{
  font-size: 12px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.btn_menu_mob{
  display: none;
}

.nav_desktop{
  display: flex;
}

.box_category{
  width: 82% !important;
  /*height: 10rem;*/
  display: flex !important;
  flex-direction: row;
  justify-content: space-between !important;
  font-size: 12px;
  color: #454545;
  /* margin-top: 50px; */
}
.items_category{
  position: relative;
  width:  160px;
  padding: 20px;
  gap: 10px;
  height: 160px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: end;
  background: #FFFFFF;
  box-shadow: 5px 10px 30px -15px rgba(0, 0, 0, 0.1);
  border-radius: 15px;
}
.img_category{
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 60px;
  height: auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

.display_desc_sell{
  display: flex;
}
.display_mob_sell{
  display: none;
}

/************************************ search form ****************************************/

.form-control::placeholder {
  color: #a6b8ba !important;
}

.form-control{
  background: #FFFFFF;
  box-shadow: 5px 8px 30px -15px rgba(0, 0, 0, 0.1);
  direction: rtl;
  color:black;
  border: 0;
  border-radius: 4px!important;
  height: 45px

}

.form-control:focus{
  color:black;
  box-shadow:unset;
  background: #FFFFFF;
}

/************************************ Box ****************************************/

@media only screen and (max-width: 1199px) {
  .input_search {
    max-width: 35%;
  }
  .display_btn_nav_desc{
    display: none!important;
  }
  .display_btn_nav_mobile{
    display: flex!important;
  }
  .navbar {
    width: 100%;
  }

  .nav_desktop{
    display: none;
  }
  
  .btn_menu_mob{
    display: block;
    height: 55px;
    width: 60px;
    border-radius: 15px;
    font-size: 14px;
  }
  .nav_mobile_items{
    width: 0;
    height: 0;
    overflow: hidden;
  }
  .offcanvas{
    height: 75%!important;
  }
}
@media only screen and (max-width: 992px) {
  .content_box_sec1{
    margin-top: 0 !important;
  }
}
@media only screen and (max-width: 767px) {
  .display_span_sell{
    display: none!important;
  }

  .display_desc_sell{
  display: none !important;
  }
  .display_mob_sell{
    display: flex !important;
  }
  .navbar {
    width: 100%;
  }  .nav_mobile_items{
       width: 0;
       height: 0;
       overflow: hidden;
     }
}
@media only screen and (max-width: 500px) {
  .navbar {
    width: 100%;
  }
  .nav_mobile_items{
    width: 0;
    height: 0;
    overflow: hidden;
  }
}
@media only screen and (max-width: 575px) {

  .input_mob{
    display: flex!important;
  }
  .input_desktop{
    display: none!important;
  }
  .input_search {
    max-width: 100%;
  }
  .nav_mobile_items{
    width: 0;
    height: 0;
    overflow: hidden;
  }
}
</style>

<script>
 
import swiper from "@/components/helperComponents/swiper.vue";

export default {
  data() {
    return {
      count: 0,
      dataMenu:[
        {
          text:"ابزار جراحی",
          href:"#",
          key:0
        },
        {
          text:"اتاق عمل",
          href:"#",
          key:1
        },
        {
          text:"تجهیزات پزشکی عمومی",
          href:"#",
          key:2
        },
        {
          text:"هتلینگ",
          href:"#",
          key:3
        },
        {
          text:"تخصصی",
          href:"#",
          key:4
        },
        {
          text:"فیزیوتراپی و توانبخشی",
          href:"#",
          key:5
        },
        {
          text:"تصویربرداری",
          href:"#",
          key:6
        },
        {
          text:"استریلیزاسیون و لندری",
          href:"#",
          key:7
        },
        {
          text:"لوازم مصرفی پزشکی و بیمارستانی",
          href:"#",
          key:8
        },
        {
          text:"تجهیزات آزمایشگاهی",
          href:"#",
          key:9
        },
      ],
      dataCategory:[
        {
          text:"دستگاه های پزشکی",
          img:"./src/assets/img/category%20img/CT Scanner.svg",
          href:"#",
          key:0
        },
        {
          text:"تجهیزات اتاق عمل",
          img:"./src/assets/img/category%20img/Catheter.svg",
          href:"#",
          key:1
        },
        {
          text:"روپوش های پزشکی",
          img:"./src/assets/img/category%20img/Hospital Gown.svg",
          href:"#",
          key:2
        },
        {
          text:"تخت های بیمارستانی",
          img:"./src/assets/img/category%20img/Hospital Wheel Bed.svg",
          href:"#",
          key:3
        },
        {
          text:"ابزار پزشکی",
          img:"./src/assets/img/category%20img/Stethoscope.svg",
          href:"#",
          key:4
        },
      ]
    }
  },
  components:{
    swiper
  },

}
</script>

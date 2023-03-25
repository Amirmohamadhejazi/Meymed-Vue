<template>
  <div class="d-flex justify-content-center flex-column bg_White trn3 container  ">
    <Header/>
    <Sec1/>
    <Sec2/>
    <Sec3/>
    <Sec4_6 typeCmp="sec4"/>
    <Sec5/>
    <Sec4_6 typeCmp="sec6"/>
    <Sec7/>
    <Sec8/>
    <Footer/>
  </div>
</template>
<script>
import Header from "@/components/home/header.vue";
import Sec1 from "@/components/home/section1.vue";
import Sec2 from "@/components/home/section2.vue";
import Sec3 from "@/components/home/section3.vue";
import Sec4_6 from "@/components/home/section4_6.vue";
import Sec5 from "@/components/home/section5.vue";
import Sec7 from "@/components/home/section7.vue";
import Sec8 from "@/components/home/section8.vue";
import Footer from "@/components/footer/Footer.vue";

export default {
  data() {
    return {
      count: 0,
      timeCount : {},
    }
  },
  components:{
    Header,
    Sec1,
    Sec2,
    Sec3,
    Sec5,
    Sec4_6,
    Sec8,
    Sec7,
    Footer,
  },
}

</script>
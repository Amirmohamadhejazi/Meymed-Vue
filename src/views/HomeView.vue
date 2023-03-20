
<template>
  <div class="d-flex justify-content-center flex-column bg_White trn3 container  ">
      <Header/>
      <Sec1/>
  </div>
</template>
<script  >
import Header from "@/components/home/header.vue";
import Sec1 from "@/components/home/section1.vue";


export default {
  data() {
    return {
      count: 0,
      timeCount : {},
    }
  },
  components:{
    Header,
    Sec1
  },


  methods: {
    getTime(){
      let countDownDate = new Date("march 19, 2023 15:37:25").getTime();
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
    // this.getTime();
  },
}



</script>

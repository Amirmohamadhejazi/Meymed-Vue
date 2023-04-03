<template>
  <div class="w-100 h-100 d-flex flex-column">
    <div :class="index!== 0 ?'clp_cmp mt-5' :'clp_cmp'" v-for="(items , index) in items_collapse">
      <div class="w-100 d-flex flex-column justify-content-center">
          <div class="w-100 d-flex justify-content-between align-items-center">
            <div class="d-flex flex-row align-items-center" >
              <span class="text_index">{{index+1}}</span>
              <span class="mx-1 text-title">{{items.title}}</span>
            </div>
            <div class=" icon_clp_box" @click="toggle(index)">
                <span :class=" show === index ? 'flex-center rotate icon_clp' :'flex-center icon_clp'">+</span>
            </div>
          </div>
          <div ref="content" v-show="show === index">
            <div class="box_clp">
              {{items.desc}}
            </div>
          </div>
      </div>
    </div>

  </div>

</template>

<script>
export default {
  props: {
    items_collapse: Array
  },
  data() {
    return {
      show: false,
      // animate: false
    }
  },
  methods: {
    toggle(index) {
      if (index === this.show){
        this.show = false
      }else {this.show = index;}
    }
  }

}
</script>

<style>

.box_clp{
  width: 100%;
  height: auto;
  padding: 20px;
  /*background:red;*/
}

.icon_clp_box {
  position: absolute;
  left: 0;
  font-size: 30px;
  background: #DEEFF5;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  transition: 0.3s;
}
.icon_clp  {
  transition: 0.3s;
}
 

.rotate {
  transform-origin: center;
  transform: rotate(45deg);

}

.clp_cmp{
  position: relative;
padding: 30px;
width: 100%;
display: flex;
justify-content: space-between;
align-items: center;
background: #FFFFFF;
box-shadow: 5px 10px 30px -15px rgba(0, 0, 0, 0.1);
border-radius: 15px;
  color: #374957;
 }

.text_index{
font-size: 36px;
text-align: center;
color: #ECECEC;
}
.text-title{
  font-weight: 400;
  font-size: clamp(13px , 1rem , 1vw);
  color: #000000;

}
</style>

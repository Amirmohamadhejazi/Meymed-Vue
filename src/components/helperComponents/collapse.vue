<template>
  <div class="w-100 h-100 d-flex flex-column">
    <div :class="index!== 0 ?'clp_cmp mt-5' :'clp_cmp'" v-for="(items , index) in items_collapse">
      <div class="w-100 d-flex flex-column justify-content-center">
          <div class="w-100 d-flex justify-content-between align-items-center">
            <div class="d-flex flex-row align-items-center" >
              <span class="text_index">{{index+1}}</span>
              <span class="me-4 text-title">{{items.title}}</span>
            </div>
            <div class="icon_clp" @click="toggle(index)">
              <div :class="{ 'rotate': show }">
                <span v-if="show === index ">+</span>
                <span v-else>&times;</span>
              </div>
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

.icon_clp {
  font-size: 30px;
  background: #DEEFF5;
  min-width: 50px;
  min-height: 50px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}


.rotate {
  transform: rotate(0);
}

.clp_cmp{
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
  font-size: 18px;
  color: #000000;

}
</style>

<template>
  <h1>sec 2</h1>
</template>

<style>
/************************************ Box ****************************************/



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

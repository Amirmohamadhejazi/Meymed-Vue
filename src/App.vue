<template>
<!--  <nav>-->
<!--    <RouterLink to="/">Home</RouterLink>-->
<!--    <RouterLink to="/about">About</RouterLink>-->
<!--  </nav>-->
  <RouterView />
</template>
<script>
import { RouterView } from 'vue-router'
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'

export default {
  data() {
    return {
      count: 0
    }
  },
  components:{
    // HelloWorld,
    // RouterLink,
    RouterView
  }
}
</script>

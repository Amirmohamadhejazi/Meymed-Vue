<template>
  <RouterView />
</template>
<script>
import { RouterView } from 'vue-router'
export default {
  data() {
    return {
      count: 0
    }
  },
  components:{
    RouterView
  }
}
</script>
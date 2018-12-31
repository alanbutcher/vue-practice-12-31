<template>
  <div id="app">
    <app-header></app-header>
    <div>{{ name }}</div>
  <compFooter></compFooter>
  </div>
</template>



<script>
import compFooter from  './components/Header_footer/Footer.vue'

export default {
  data() {
    return {
      name: "Alan"
    }
  },
  components: {
    compFooter
    }
}


</script>




<style>

</style>

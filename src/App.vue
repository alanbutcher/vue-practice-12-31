<template>
  <div id="app">
    <app-header></app-header>
    <div>{{ name }}</div>
    <app-footer></app-footer>
  </div>
</template>



<script>
import Footer from  './components/Header_footer/Footer.vue'

export default {
  data() {
    return {
      name: "Alan"
    }
  },
  components: {
    'app-footer': Footer
    }
}


</script>




<style>

</style>

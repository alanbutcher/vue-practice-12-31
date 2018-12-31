<template>
  <div id="app">
    <app-header></app-header>
    <div class="container">
      <div>{{ name }}</div>
    </div>
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

body {
  padding: 0;
  margin: 0;
  font-family: 'Roboto', sans-serif;
}
.container {
  min-height: 84vh;
  box-sizing: border-box;
  padding: 20px;
}
</style>

<template>
  <div id="app">
    <app-header></app-header>
    <compUserProfile
      :userName="name"
      :userLastname="lastname"
      :userAge="age"
      :userParents="parents"
      @updateName="name = $event"
      :updateLastname="updateLastname"
    ></compUserProfile>
    <compFooter></compFooter>
  </div>
</template>



<script>
import compFooter from  './components/Header_footer/Footer.vue';
import compUserProfile from './components/User/Profile.vue';

export default {
  data() {
    return {
      name: "Alan",
      lastname: "Butcher",
      age: 1,
      parents: {
        mother: "Maddy",
        father: "Alan"
      }
    }
  },

  components: {
    compFooter,
    compUserProfile
    },

  methods: {
    updateLastname(value) {
      this.lastname = value
    }
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

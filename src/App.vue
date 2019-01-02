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
    <compAbilities>
      <ul slot='main_ab'>
        <li>HTML</li>
        <li>CSS</li>
        <li>JS</li>
      </ul>
      <div slot='notes'>
        <p>Also know Vue</p>
      </div>
      <div>
        <a href="#">See more about this user</a>
      </div>
      <div :slot='slotName'>
        other content
      </div>
    </compAbilities>
    <compFooter></compFooter>
  </div>
</template>



<script>
import compFooter from  './components/Header_footer/Footer.vue';
import compUserProfile from './components/User/Profile.vue';
import compAbilities from './components/User/Abilities.vue'; 

export default {
  data() {
    return {
      name: "Alan",
      lastname: "Butcher",
      age: 1,
      parents: {
        mother: "Maddy",
        father: "Alan"
      },
      slotName:''
    }
  },

  components: {
    compFooter,
    compUserProfile,
    compAbilities
    },

  created() {
    setTimeout(() => {
      this.slotName = 'other'
    }, 3000)
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

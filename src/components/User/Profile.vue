<template>
  <div class="contianer">
    <div class="user_profile">
      <h3>User Information:</h3>
      <ul>
        <li><span>Name:</span> {{ userName }} </li>
        <li><span>Last Name:</span> {{ userLastname }} </li>
        <li><span>Age:</span> {{ userAge }} </li>
      </ul>
      <h3>Parents</h3>
      <ul>
        <li v-for="(key, value, index) in userParents" :key="index">
          <span>{{ key }}: </span>
          {{ value }}
        </li>  
      </ul>
    </div>
    <button @click="updateName">Update Name</button>
    <button @click="updateLastname('Bear')">Update Last Name</button>
  </div>
</template>

<script>
  export default {
    props: {
      userName: String,
      userLastname: String,
      userAge: Number,
      userParents: Object,
      updateLastname: Function
    },
    methods: {
      updateName() {
        this.$emit('updateName', 'Walter')
      }
    }
  }
</script>

<style>
  span {
    font-weight: 800;
  }
  .user_profile {
    border: 2px solid #2196F3;
    padding: 10px 20px;
  }
</style>
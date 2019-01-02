<template>
  <div class="user_profile">
    <h3>User Profile:</h3>
    <hr>
    <slot name='other'>Loading...</slot>
    <hr>
    <div>
      <slot name='main_ab'></slot>
    </div>
    <slot name='notes'></slot>
    <hr>
    <slot></slot>
    <hr>
  </div>
</template>


<script>
  export default {
    data() {
      return {
        abilities:['HTML', 'CSS', 'JS']
      }
    }
  }
</script>


<style scoped>
  li {
    color: red;
  }
  .user_profile {
    border: 2px solid #2196F3;
    padding: 10px 20px;
  }
</style>
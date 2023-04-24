<template>
  <div class="Profile">

    <h1>This is an Profile page</h1>
    <p>Profile ID: {{ userId }}</p>

  </div>
</template>

<script>
export default {
  name: 'Profile',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      userId: this.$route.params.user_id
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

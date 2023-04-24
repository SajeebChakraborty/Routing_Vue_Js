<template>
  <div class="Navbar">

    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link :to="{name: 'Contact'}">Contact</router-link>
    </nav>
  <div>
    <ul>
        <li v-for="(id,index) in userIds" :key="index">
          <router-link :to="{ name: 'Profile', params: {user_id: id} }">User {{ id }}</router-link>
        </li>
    </ul>
    <button @click="Contact">Contact</button>

  </div>

  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      userIds: ['1', '2', '3', '4', '7', '11']
    }
  },
  methods: {
    Contact () {
      this.$router.push({ name: 'Contact' })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

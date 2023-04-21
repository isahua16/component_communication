<template>
  <div id="app">
    <small-user-profile :users="users"></small-user-profile>
  </div>
</template>

<script>
import SmallUserProfile from '@/components/SmallUserProfile.vue'

export default {
  name: 'App',
  components: {
    SmallUserProfile
  },
  data() {
    return {
      users: [
        {
          name: `name_one`,
          age: 29,
          is_premium: true,
          id: 1
        },
        {
          name: `name_two`,
          age: 16,
          is_premium: false,
          id: 2
        }
      ],
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

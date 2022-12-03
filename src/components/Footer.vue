<script>
export default {
  name: 'Footer',
  computed: {
    aboutPage() {
        if (this.$route.path === '/about') {
            return true
        } else {
            return false
        }
    },
    homePage() {
        if (this.$route.path === '/') {
            return true
        } else {
            return false
        }
    }
  }
}
</script>

<template>
  <footer>
    <p>Copyright &copy; {{ new Date().getFullYear() }}</p>
    <router-link v-show="homePage" to="/about">About</router-link>
    <router-link v-show="aboutPage" to="/">Home</router-link>
  </footer>
</template>

<style scoped>
a {
  color: #333;
}
footer {
  margin-top: 30px;
  text-align: center;
}
</style>
<template>
  <header>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="danger">
      <b-navbar-brand href="#">NuxtJs</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item><nuxt-link to="/">Home</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="/users">Users</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="/about">About</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="/login">Login</nuxt-link></b-nav-item>
          <b-nav-item v-if='isAuth'><a class='nav-link' href='#' @click.prevent='logout'>Logout</a></b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
  </header>
</template>

<script>
export default {
  name: 'Navbar',
  computed: {
    isAuth() {
      return this.$store.getters.isAuth
    }
  },

  methods: {
    logout() {
      this.$store.dispatch('logout')
    }
  }
}
</script>

<style scoped>

</style>

<template>
  <section>
    <h1>{{ pageTitle }}</h1>
    <ul>
      <li v-for='user of users' :key='user.id'>
        <a href='#' @click.prevent='goTo(user)'>{{user.name}} {{user.email}}</a>
      </li>
    </ul>
  </section>
</template>

<script>
// import error from '~/layouts/error'

export default {
  name: 'index',
  // async asyncData({store, error}) {
  //   try {
  //     await store.dispatch('user/fetchUsers')
  //     return {}
  //   }catch (e) {
  //     error(e)
  //   }
  // },
  // async fetch({ store, error }) {// чтобы не возвращать пустой обЪект fetch
  //   try {
  //     if (store.getters['user/users'].length === 0) {
  //       await store.dispatch('user/fetchUsers')
  //     }
  //   }catch (e) {
  //     error(e)
  //   }
  // },

  data() {
    return {
      pageTitle: 'This is users page'
    }
  },

  computed: {
    users() {
      return this.$store.getters['user/users']
    }
  },

  methods: {
    goTo (user) {
      this.$router.push('/users/' + user.id)
    }
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  padding-top: 30vh;
}
</style>

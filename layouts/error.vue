<template>
  <section>
    <h1>Error 404</h1>
    <nuxt-link to='/'>Home</nuxt-link>
  </section>
</template>

<script>
export default {
  name: 'error'
}
</script>

<style scoped>
h1 {
  color: red;
}
section {
  display: flex;
   /*justify-content: center; */
  flex-direction: column;
  align-items: center;
}
</style>

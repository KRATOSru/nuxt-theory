<template>
  <section>
    <h1>This is About page</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae, voluptatem.</p>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ducimus et harum laudantium optio perspiciatis quod.</p>
  </section>
</template>

<script>
export default {
  name: 'index',
  middleware: ['auth']
}
</script>

<style scoped>
h1 {
  text-align: center;
  padding-top: 30vh;
}
</style>

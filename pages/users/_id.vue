<template>
  <div>
    <h1>{{user.name}}</h1>
    <hr>
    <b>{{user.email}}</b>
  </div>
</template>

<script>
export default {
  name: '_id',
  validate({params}) {
    return /^\d+$/.test(params.id)
  },
  async asyncData({params, error, store}) {
    try {
      const user = await store.dispatch('user/fetchUserById', params.id)
      return {user}
    } catch (e) {
      error(e)
    }
  }
}
</script>

<template>
  <div>
    <h1 v-if="error.statusCode === 404">Not found Request page...</h1>
    <h1 v-else-if="error.statusCode === 500">Internal error!!</h1>
    <h1 v-else>An unexpected error has occurred</h1>
    <nuxt-link to="/">Home</nuxt-link>
  </div>
</template>

<script>
export default {
  name: 'error',
  props: ['error']
}
</script>
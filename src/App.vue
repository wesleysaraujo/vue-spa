<template>
  <div id="app">
    <list-products></list-products>
  </div>
</template>

<script>
import ListProducts from './components/ListProducts.vue'

export default {
  components: {
    ListProducts
  }
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
}
</style>

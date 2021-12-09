<template>
  <div id="app">
    <Disclaimer />
    <Header />
    <Products />
  </div>
</template>

<script>
import Products from './components/Products.vue'
import Header from './components/Header.vue'
import Disclaimer from './components/Disclaimer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Products,
    Disclaimer
  }
}
</script>
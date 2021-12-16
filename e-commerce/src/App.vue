<template>
  <div id="app">
    <div v-if="!disclaimerAcknowledged">
        <Disclaimer @acknowledge-disclaimer="acknowledgeDisclaimer" />
    </div>
    <div v-else>
      <Header />
      <Products />
    </div>
  </div>
</template>

<script>
import Products from './components/Products.vue'
import Header from './components/Header.vue'
import Disclaimer from './components/Disclaimer.vue'

export default {
  name: 'App',
  data(){
    return {
      disclaimerAcknowledged: false
    }
  },
  components: {
    Header,
    Products,
    Disclaimer
  },
  methods: {
    acknowledgeDisclaimer(){
      this.disclaimerAcknowledged = true
    }
  }
}
</script>
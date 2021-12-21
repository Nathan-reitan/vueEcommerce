<template>
  <div id="app">
    <div v-if="!disclaimerAcknowledged">
        <Disclaimer @acknowledge-disclaimer="acknowledgeDisclaimer" />
    </div>
    <div v-else>
      <Header />
      <Main />
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Disclaimer from './components/Disclaimer.vue'

export default {
  name: 'App',
  data(){
    return {
      disclaimerAcknowledged: false,
    }
  },
  components: {
    Header,
    Main,
    Disclaimer
  },
  methods: {
    acknowledgeDisclaimer(){
      this.disclaimerAcknowledged = true
    }
  }
}
</script>
<template>
    <div class="disclaimer">
        <h3>
            This site is for demonstrative purposes only, nothing is actually for sale. 
        </h3>
        <h3>
            DO NOT ENTER ANY CREDIT CARD OR PERSONAL INFORMATION INTO THIS SITE.
        </h3>
        <h3>
            To continue to site please acknowledge the disclaimer by clicking the acknowledge button below.
        </h3>
        <button @click="onClick()" class="acknowledgeBtn">
            Acknowledge
        </button>
    </div>
</template>

<script>
export default {
  name: 'Disclaimer',
  props: {
    
  },
  methods: {
      onClick(){
          this.$emit('acknowledge-disclaimer')
      }
  }
}
</script>
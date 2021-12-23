<template>
    <div>
        <button @click="onClick" class="goBack">Go Back</button>
        <h1>{{title}}</h1>
        <img :src="image" :alt="altText" />
        <p>{{description}}</p>
    </div>
</template>

<script>
export default {
  name: 'ProductDetails',
  props: {
    title: {
      required: true,
      type: String,
    },
    description: {
      required: true,
      type: String,
    }, 
    image: {
      required: true,
      type: String,
    }, 
    altText: {
      required: true,
      type: String,
    },
  },
  methods: {
    onClick(){
          this.$emit('clear-details')
      }
  }
  
}
</script>
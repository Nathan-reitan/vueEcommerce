<template>
    <main>
        <Products v-if="!details" @send-details="sendDetails"/>
        <ProductDetail v-else v-bind="product" @clear-details="clearDetails"/>
    </main>
</template>

<script>
import Products from './Products.vue'
import ProductDetail from './ProductDetail.vue'

export default {
    name: 'Main',
    data(){
        return {
            details: false,
            product: {
                title: null,
                description: null,
                image: null,
                altText: null,
            },
        }
    },
    components: {
    Products,
    ProductDetail
    },
    methods: {
        sendDetails(details){
            this.details = true;
            this.product.title = details.title;
            this.product.description = details.description;
            this.product.image = details.image;
            this.product.altText = details.altText;
        },
        clearDetails(){
            this.details = false;
            this.title = null;
            this.description = null;
            this.image = null;
            this.altText = null;
        }
    }
    
}


</script>
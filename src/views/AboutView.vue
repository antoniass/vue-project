<!-- Produkt sida -->
<script setup>
// Hämta produktkort, komponent
import ProductCard from "../components/ProductCard.vue"
</script>
<template>
    <h3 class="title text-center">{{ title }}</h3>

    <div class="container text-center">
        <div class="row align-items-start">
            <product-card v-for="product in products" :key="product.id" :prod="product" />
        </div>
</div>
</template>

<script>
// Hämta data ifrån json
export default {
    data() {
        return {
            title: "Drycker",
            products: []
        }
    },
    name: 'AboutView',
    components: { 'product-card': ProductCard },
    mounted() {
        this.fetchData()
    },
    methods: {
        async fetchData() {
            const res = await fetch('products.json')
            const result = await res.json()
            this.products = result
        }
    }
}
</script>

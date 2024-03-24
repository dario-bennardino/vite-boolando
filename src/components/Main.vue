<script>
import db from '../assets/data/db';
import ProductCard from './partials/ProductCard.vue';
    export default {
        components:{
            ProductCard
        },
        data(){
            return{
                products: db.products
            };
        }
    }
</script>

<template>
    <main>
        <div class="container">
            <ProductCard v-for="product in products" :key="product.id" :product="product"/>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    .container {
        display: flex;
        justify-content: center;
        width: 80%;
        max-width: 1000px;
        margin: 40px auto;
        flex-wrap: wrap;
        align-content: start;
        justify-content: space-between;
    }
</style>
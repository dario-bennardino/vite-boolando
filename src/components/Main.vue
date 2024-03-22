<script>
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
            <ProductCard v-for="(product, index) in products" :key="index" :product="product"/>
           


            <!-- <div class="product">
                <div class="top-product">
                    <img src="/public/assets/img/1.webp" alt="img1">
                    <div class="discount md">-50%</div>
                    <div class="sostenibilità">Sostenibilità</div>
                    <div class="preferiti">&hearts;</div>
                </div>
                <div class="bottom-product">
                    <div class="marca">Levi's</div>
                    <div class="articolo">RELAXED FIT TEE UNISEX</div>
                    <div class="prezzi">
                        <div class="prezzo-scontato">14.99€</div>
                        <div class="prezzo-pieno">29.99€</div>
                    </div>
                </div>
            </div>
            <div class="product">
                <div class="top-product">
                    <img src="/public/assets/img/2.webp" alt="img2">
                    <div class="discount sm">-30%</div>
                    <div class="preferiti">&hearts;</div>
                </div>
                <div class="bottom-product">
                    <div class="marca">Guess</div>
                    <div class="articolo">ROSES TEE</div>
                    <div class="prezzi">
                        <div class="prezzo-scontato">20.99€</div>
                        <div class="prezzo-pieno">29.99€</div>
                    </div>
                </div>
            </div>
            <div class="product">
                <div class="top-product">
                    <img src="/public/assets/img/3.webp" alt="img3">
                    <div class="discount sm">-30%</div>
                    <div class="preferiti">&hearts;</div>
                </div>
                <div class="bottom-product">
                    <div class="marca">Come zucchero filato</div>
                    <div class="articolo">VOGLIA DI COLORI PASTELLO</div>
                    <div class="prezzi">
                        <div class="prezzo-scontato">14.99€</div>
                        <div class="prezzo-pieno">29.99€</div>
                    </div>
                </div>
            </div>
            <div class="product">
                <div class="top-product">
                    <img src="/public/assets/img/4.webp" alt="img4">
                    <div class="discount md">-50%</div>
                    <div class="sostenibilità">Sostenibilità</div>
                    <div class="preferiti">&hearts;</div>

                </div>
                <div class="bottom-product">
                    <div class="marca">Levi's</div>
                    <div class="articolo">TEE UNISEX</div>
                    <div class="prezzi">
                        <div class="prezzo-scontato">14.99€</div>
                        <div class="prezzo-pieno">29.99€</div>
                    </div>
                </div>
            </div>
            <div class="product">
                <div class="top-product">
                    <img src="/public/assets/img/5.webp" alt="img5">
                    <div class="preferiti">&hearts;</div>
                </div>
                <div class="bottom-product">
                    <div class="marca">Come zucchero filato</div>
                    <div class="articolo">VOGLIA DI COLORI PASTELLO</div>
                    <div class="prezzi">
                        <div class="prezzo-scontato">99.99€</div>
                    </div>
                </div>
            </div>
            <div class="product">
                <div class="top-product">
                    <img src="/public/assets/img/6.webp" alt="img6">
                    <div class="sostenibilità-singolo">Sostenibilità</div>
                    <div class="preferiti">&hearts;</div>
                </div>
                <div class="bottom-product">
                    <div class="marca">Espirit</div>
                    <div class="articolo">MAGLIONE - BLACK</div>
                    <div class="prezzi">
                        <div class="prezzo-scontato">29.99€</div>
                    </div>
                </div>
            </div> -->

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
        .product {
            margin: 10px;
            width: 300px;
            .top-product {
                position: relative;
                img{
                    max-width: 100%;
                }
                .discount {
                    position: absolute;
                    left: 0;
                    bottom: 30px;
                    padding: 5px;
                    font-size: 0.6rem;
                }
                .md {
                    background-color: green;
                    color: white;
                }
                .sm {
                    background-color: red;
                    color: white;
                }
                .sostenibilità {
                    position: absolute;
                    bottom: 30px;
                    left: 38px;
                    background-color: green;
                    color: white;
                    font-size: 0.6rem;
                    padding: 5px;
                }
                .sostenibilità-singolo {
                    position: absolute;
                    bottom: 30px;
                    left: 0;
                    background-color: green;
                    color: white;
                    font-size: 0.6rem;
                    padding: 5px;
                }
                .preferiti {
                    background-color: white;
                    padding: 5px 7px;
                    color: black;
                    position: absolute;
                    right: 0;
                    top: 5px;
                    display: none;
                }
            }
            .bottom-product{
                .marca {
                    font-size: 0.9rem;
                }
                .articolo {
                    font-weight: bold;
                }
                .prezzi {
                    display: flex;
                        .prezzo-scontato {
                            color: red;
                            font-weight: bold;
                        }
                        .prezzo-pieno {
                            text-decoration: line-through;
                            padding-left: 5px;

                        }
                }

            }

        }

    }
</style>
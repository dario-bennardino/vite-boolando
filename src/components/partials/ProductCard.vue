<script>
    export default {
        props:{
            product: {
                type: Object,
                required: true,
            }
        },
        methods:{
            getImagePath: function () {
                return '/assets/img/' + this.product.frontImage;
            }
        }
    }
</script>

<template>
    <div class="product">
                <div class="top-product">
                    <img :src="getImagePath()" :alt="product.frontImage">
<!--                     <div class="discount md">{{ product.badges.value }}</div>
                    <div class="sostenibilità">Sostenibilità</div> -->
                    <div v-if="product.isInFavorites" class="preferiti">&hearts;</div>
                </div>
                <div class="bottom-product">
                    <div class="marca">{{ product.brand }}</div>
                    <div class="articolo">{{ product.name }}</div>
                    <div class="prezzi">
<!--                         <div class="prezzo-scontato">14.99€</div> -->
                        <div class="prezzo-pieno">{{ product.price }}€</div>
                    </div>
                </div>
            </div>
</template>

<style lang="scss" scoped>
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
            // display: none;
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
</style>
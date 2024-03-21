<script>
    export default {
        
    }
</script>

<template>
    <header>
        <div class="container-homepage">
            <div class="topbar">
                <div class="genere">
                    <a href="">Donna</a>
                    <a href="">Uomo</a>
                    <a href="">Bambino</a>
                </div>
                <div class="logo">
                    <img src="/public/assets/img/boolean-logo.png" alt="logo">
                </div>
                <div class="social">
                    <i class="fa-regular fa-user"></i>
                    <i class="fa-regular fa-heart"></i>
                    <i class="fa-solid fa-bag-shopping"></i>
                </div>
            </div>

        </div>
    </header>
</template>

<style lang="scss" scoped>
  header {
    background-color: #FF6902;
    height: 100px;
    display: flex;
    justify-content: center;
    justify-content: space-between;
    box-shadow: 0 1px 3px;

        .container-homepage {
            width: 80%;
            max-width: 1000px;
            margin: 40px auto;
            align-items: center;
            .topbar {
                display: flex;
                justify-content: center;
                justify-content: space-between;
                align-items: center;
                // .social i {
                //     color: white;
                //     padding: 5px;
                // }
                .social{
                    i{
                        color: white;
                        padding: 5px;
                    }
                }
                .genere>a {
                    color: white;
                    text-decoration: none;
                    font-weight: bold;
                    padding: 5px;

                }
                .logo>img {
                    width: 150px;
                }



            }  

        }
    
    
    
    }
</style>
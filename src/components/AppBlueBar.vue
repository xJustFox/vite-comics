<script>
    export default {
        name: 'AppBlueBar',
        data() {
            return {
                arr:[
                    {
                        icon: '/src/assets/imgs/buy-comics-digital-comics.png',
                        title: 'DIGITAL COMICS',
                    },
                    {
                        icon: '/src/assets/imgs/buy-comics-merchandise.png',
                        title: 'DC MERCHANDISE',
                    },
                    {
                        icon: '/src/assets/imgs/buy-comics-subscriptions.png',
                        title: 'SUBSCRIPTIONS',
                    },
                    {
                        icon: '/src/assets/imgs/buy-comics-shop-locator.png',
                        title: 'COMIC SHOP LOCATIOR',
                    },
                    {
                        icon: '/src/assets/imgs/buy-dc-power-visa.svg',
                        title: 'DC POWER VISA',
                    }
                ]
            }
        },
    }
</script>

<template>
    <section class="shippingBanner">
        <div class="container">
            <ul class="list-unstyled m-0  d-flex justify-content-around  p-5 flex-wrap">
                <li v-for="(item, index) in arr" :key="index">
                    <img :src="item.icon" alt="">
                    <span class="title">{{item.title}}</span>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/_variables.scss' as *; 
    .shippingBanner{
        background-color: $my_blue;
        color: #fff;
        li{
            &:hover{
                cursor: pointer;

                img{
                    transform: scale(1.1);
                }
            }

            img{
                height: 50px;
            }
    
            .title{
                font-size: smaller;
                padding: 0 10px;
            }
        }
    }
</style>
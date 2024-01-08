<script>
import AppBlueBar from './AppBlueBar.vue';

export default {
    name:'AppFooter',
    components: {
        AppBlueBar
    },
    data() {
        return {
            arrList: [
                {
                    title: "DC COMICS",
                    links: ["Characters", "Comics", "Movies","Tv", "Games","Videos", "News"],
                },
                {
                    title: "SHOP",
                    links: ["Shop DC", "Shop DC Collectibles"],
                },
                {
                    title: "DC",
                    links: ["Terms Of Use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
                },
                {
                    title: "SITES",
                    links: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"],
                },
            ],
            arrSocial: [
                {
                    alt: "Faceboock",
                    img: "/src/assets/imgs/footer-facebook.png",
                },
                {
                    alt: "Twitter",
                    img: "/src/assets/imgs/footer-twitter.png",
                },
                {
                    alt: "YouTube",
                    img: "/src/assets/imgs/footer-youtube.png",
                },
                {
                    alt: "Pinterest",
                    img: "/src/assets/imgs/footer-pinterest.png",
                },
                {
                    alt: "Periscope",
                    img: "/src/assets/imgs/footer-periscope.png",
                },
            ]
        }
    },
}
</script>

<template lang="">
    <footer>
        <!-- Blue Bar -->
        <AppBlueBar />

        <!-- Info List -->
        <div class="container ">
            <div class="row">

                <div class="col">
                    <div>
                        <div class="row flex-column content">
                            <div class="col-4" v-for="(item, index) in arrList" :key="index">
                                <a class="title" href="#">{{item.title}}</a>
    
                                <div v-for="(link, index) in item.links" :key="index">
                                    <a class="my-gray" href="#">{{link}}</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col content overflow-hidden">
                    <img class="log-bg" src="../assets/imgs/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>

        <!-- Button and Socials -->
        <div class="my-bg-black">
            <div class="container">
                <div class="row justify-content-between py-4">
                    <div class="col">
                        <button class="btn my-btn text-white">SING-UP NOW!</button>
                    </div>
                    <div class="col d-flex justify-content-end ">
                        <ul class="list-unstyled m-0 d-flex align-items-center">
                            <li>FOLLOW US</li>
                            <li v-for="(social, index) in arrSocial" :key="index">
                                <img :src="social.img" :alt="social.alt">
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/_variables.scss' as *;

    footer{
        background-image: url("../assets/imgs/footer-bg.jpg");
        background-size: cover;

        .content{
            height: 450px;
            padding: 50px 0;
        }
        .title{
            color: #fff;
            font-size: 30px;
            font-weight: bolder;
        }

        .my-gray{
            color: #878484fa;
        }

        .log-bg{
            position: relative;
            bottom: 30%;
        }

        .my-bg-black{
            background-color: $my-black;

            .my-btn{
                border: 2px solid $my_blue;
                border-radius: 0;
            }

            ul li:first-child{
                font-weight: bolder;
                color: $my_blue;
            }

            ul li{
                padding: 0 10px;
            }
        }
    }

</style>
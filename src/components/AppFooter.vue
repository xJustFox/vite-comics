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
                    href: "#",
                },
                {
                    alt: "Twitter",
                    img: "/src/assets/imgs/footer-twitter.png",
                    href: "#",
                },
                {
                    alt: "YouTube",
                    img: "/src/assets/imgs/footer-youtube.png",
                    href: "#",
                },
                {
                    alt: "Pinterest",
                    img: "/src/assets/imgs/footer-pinterest.png",
                    href: "#",
                },
                {
                    alt: "Periscope",
                    img: "/src/assets/imgs/footer-periscope.png",
                    href: "#",
                },
            ]
        }
    },
}
</script>

<template>
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
                                <span class="title">{{item.title}}</span>
    
                                <div v-for="(link, index) in item.links" :key="index">
                                    <a class="infoItems" href="#">{{link}}</a>
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
                            <li class="socialIcon" v-for="(social, index) in arrSocial" :key="index">
                                <a :href="social.href">
                                    <img :src="social.img" :alt="social.alt">
                                </a>
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
            cursor: default;
            color: #fff;
            font-size: 30px;
            font-weight: bolder;
        }

        .infoItems{
            color: #878484fa;

            &:hover{
                color: $my_blue;
                cursor: pointer;
            }
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

                &:hover{
                    transform:scale(1.1);
                }
            }

            ul{
                li:first-child{
                    cursor: default;
                    font-weight: bolder;
                    color: $my_blue;
                }

                li{
                   padding: 0 10px;
               }

               .socialIcon:hover{
                transform: scale(1.1);
               }

            }
        }
    }

</style>
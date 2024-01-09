<script>
import AppJumbo from './AppJumbo.vue';
import AppCardComic from './AppCardComic.vue';

export default {
    name: 'AppMain',
    components: {
        AppJumbo,
        AppCardComic,
    },
    data() {
        return {
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]
        }
    },
}
</script>

<template>
    <main>
        <AppJumbo />
        <div class="container my-p position-relative">
            <div class="plate">CURRENT SERIES</div>

            <div class="my-row">
                <AppCardComic v-for="item in comics" :comic="item"/>
            </div>

            <div class="text-center pt-4">
                <button class="my-btn">LOAD MORE</button>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/_variables.scss' as *;
    
    main{
        background-color: #1c1c1c;


        .my-p{
            padding: 50px 0px 15px 0px;
        }
        .plate{
            position: absolute;
            bottom: 97%;
            cursor: default;
            background-color: $my-blue;
            color: #fff;
            font-size: large;
            font-weight: 900;
            padding: 8px 25px;
        }

        .my-row{
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 20px 5px;

            
        }

        .my-btn{
            background-color: $my-blue;
            border: 0;
            padding: 5px 40px;
            color: #fff;
            font-weight: 600;
            font-size: small;

            &:hover{
                transform:scale(1.1);
            }
        }

    }
</style>
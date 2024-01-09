<script>
export default {
    name: 'AppCardComic',
    props: {
        comic: Object,
    }
}
</script>

<template lang="">
    <div class="my-col">
        <div class="imgContainer">
            <img :src="comic.thumb" :alt="comic.series">
        </div>
        <div class="price">{{comic.price}}</div>
        <div class="textComics">
            {{ comic.series }}
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
    .my-col {
        width: calc(100% / 6 - 10px);
        position: relative;

        &:hover {
            cursor: pointer;

            img{
                transform: scale(1.1);
            }

        }
        
        .imgContainer {
            height: 220px;
            overflow: hidden;
            
            img {
                width: 100%;
            }
        }
        .price{
            position: absolute;
            top: 10px;
            right: 0;
            padding: 5px;
            border-radius: 10px 0 0 10px;
            background-color: rgba(57, 56, 56, 0.9);
            color: white;
        }
        
        .textComics {
            padding: 10px 0;
            color: white;
            font-size: small;
            font-weight: 600;
            text-transform: uppercase;
        }
    }
</style>
<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            links: [
                {
                    name: "CHARACTERS",
                    href: "#",
                },
                {
                    name: "COMICS",
                    href: "#",
                },
                {
                    name: "MOVIES",
                    href: "#",
                },
                {
                    name: "TV",
                    href: "#",
                },
                {
                    name: "GAMES",
                    href: "#",
                },
                {
                    name: "COLLECTIBLES",
                    href: "#",
                },
                {
                    name: "GAMES",
                    href: "#",
                },
                {
                    name: "VIDEOS",
                    href: "#",
                },
                {
                    name: "FANS",
                    href: "#",
                },
                {
                    name: "NEWS",
                    href: "#",
                },
                {
                    name: "SHOP",
                    href: "#",
                },
            ]
        }
    },
}
</script>

<template>
    <header class="py-4">
        <div class="container">
            <nav class="row align-items-center">
                <div class="col">
                    <img src="../assets/imgs/dc-logo.png" alt="">
                </div>
                <div class="col">
                    <ul class="d-flex list-unstyled m-0 ">
                        <li class="px-2 " v-for="(link, index) in links" :key="index">
                            <a :href="link.href">{{ link.name }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/_variables.scss' as *;

    img {
        height: 80px;
    }

    li a{
        font-weight: 600;

        &.active,
        &:hover{
            cursor: pointer;
            color: #0282f9;
        }
    }

</style>
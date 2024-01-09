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
    <header class="py-3">
        <div class="container">

            <!-- Nav Bar -->
            <nav class="row align-items-center">

                <!-- Logo -->
                <div class="col">
                    <a href="#">
                        <img src="../assets/imgs/dc-logo.png" alt="Logo">
                    </a>
                </div>

                <!-- Menù -->
                <div class="col">
                    <ul class="d-flex list-unstyled m-0 ">
                        <li class="px-2 " v-for="(link, index) in links" :key="index">
                            <a :href="link.href" :class="index ==  1 ? 'active' : ''">{{ link.name }}</a>
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
        color: #000;
        font-weight: 600;
        position: relative;

        &.active,
        &:hover{
            color: $my_blue;
            cursor: pointer;

            &::after{
                content: "";
                position: absolute;
                bottom: -47px;
                left: 0px;
                width: 100%;
                height: 5px;
                background-color: $my_blue;
            }
        }

    }

</style>
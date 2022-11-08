<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    title: "CHARACTERS",
                    href: "/characters",
                    active: false,
                },
                {
                    title: "COMICS",
                    href: "/comics",
                    active: true,
                },
                {
                    title: "MOVIES",
                    href: "/movies",
                    active: false,
                },
                {
                    title: "TV",
                    href: "/tv",
                    active: false,
                },
                {
                    title: "GAMES",
                    href: "/games",
                    active: false,
                },
                {
                    title: "COLLECTIBLES",
                    href: "/collectibles",
                    active: false,
                },
                {
                    title: "VIDEOS",
                    href: "/videos",
                    active: false,
                },
                {
                    title: "FANS",
                    href: "/fans",
                    active: false,
                }, {
                    title: "NEWS",
                    href: "/news",
                    active: false,
                },
                {
                    title: "SHOP",
                    href: "/shop",
                    active: false,
                }
            ]
        }
    }
}
</script>

<template>
    <header class="header">
        <div class="logo">
            <img src="../assets/vue-dc-comics-1/img/dc-logo.png" alt="Logo dc">
        </div>
        <nav class="header-navigation">
            <ul>
                <li :class="{ 'borderlist': link.active }" v-for="(link, index) in links" :key="index">
                    <a :class="{ 'active': link.active }" :href="link.href">{{ link.title }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.header {


    .logo {
        @include flex-center("horizontal");
    }

    &-navigation {
        height: 200px;

        ul {
            list-style: none;
            @include flex-center("horizontal");
            height: 100%;


            li {
                margin: 0px 1rem;
                height: 100%;

                a {

                    &:hover,
                    &.active {
                        color: lighten($primary-color, 30%);
                    }
                }
            }
        }
    }
}
</style>
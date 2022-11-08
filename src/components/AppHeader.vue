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
    <div class="background-white">
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
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.header {
    @include flex-center("horizontal");
    justify-content: space-between;
    margin: 40px auto;
    width: $container-size;
    height: 100px;


    .logo {
        @include flex-center("both");

        img {
            width: 80px;
        }
    }

    &-navigation {

        ul {
            list-style: none;
            @include flex-center("horizontal");
            height: 100%;


            li {
                @include flex-center("vertical");
                margin: 0px 1rem;
                height: 100%;
                padding-bottom: 1rem;

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
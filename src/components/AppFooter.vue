<script>
export default {
    name: "AppFooter",
    data() {
        return {
            stacks: [
                {
                    title: "CHARACTERS",
                    img: "buy-comics-digital-comics.png",
                },
                {
                    title: "DC MERCHAINDISE",
                    img: "buy-comics-merchandise.png",
                },
                {
                    title: "COMIC SHOP LOCATOR",
                    img: "buy-comics-shop-locator.png",
                },
                {
                    title: "CHARACTERS",
                    img: "buy-comics-digital-comics.png",
                },
                {
                    title: "DC POWER VISA",
                    img: "buy-dc-power-visa.svg",
                },
            ],

        }

    },
    methods: {
        getImagePath(i) {
            return new URL(`../assets/vue-dc-comics-1/img/${this.stacks[i].img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="footer-wrapper">

        <section class="blu-row">
            <div class="stack-wrapper">

                <div v-for="(stack, index) in stacks" class="stacks" :key="index">
                    <img :src="getImagePath(index)" alt="">
                    <p>{{ stack.title }}</p>
                </div>
            </div>
        </section>

        <section class="footer-links">
            <div class="links-wrapper">
                <div class="contact-links">
                    <div>
                        <h2>DC COMICS </h2>
                        <ul>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                        </ul>

                        <h2>SHOP </h2>
                        <ul>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>

                        </ul>
                    </div>
                    <div>
                        <h2>DC </h2>
                        <ul>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>

                        </ul>
                    </div>
                    <div>
                        <h2>SITES</h2>
                        <ul>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                            <li>
                                <a href=""> lorem </a>
                            </li>
                        </ul>
                    </div>

                </div>
                <div class="links-img">
                    <img src="../assets/vue-dc-comics-1/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </section>

        <section class="footer-social">

        </section>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;


.blu-row {
    background-color: #0282f9;


    .stack-wrapper {
        width: $container-size;
        margin: 0 auto;
        @include flex-direction("row");

    }
}

.footer-links {
    background-image: url(../assets/vue-dc-comics-1/img/footer-bg.jpg);
    overflow: hidden;

    .links-wrapper {
        @include flex-direction("row");
        width: $container-size;
        max-height: 300px;
        margin: 0 auto;
        align-items: center;

        .contact-links {
            @include flex-direction("row");
            @include flex-center("horizontal");

            div {
                margin: 0 1rem;
            }

            ul {
                margin: 1rem 0;
            }

            h2 {
                color: white;
            }

            a {
                color: #959595;

                &:hover {
                    color: white;
                    border-bottom: 1px solid white;
                }
            }
        }

        .links-img {

            img {
                width: 600px;
                opacity: 0.7;
            }
        }
    }
}

.footer-social {
    background-color: #303030;
    // DEBUG
    height: 100px;
}
</style>
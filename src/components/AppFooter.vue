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
            ]

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
    // DEBUG
    height: 150px;

    .stack-wrapper {
        width: $container-size;
        margin: 0 auto;
        @include flex-direction("row");

    }
}

.footer-links {
    background-image: url(../assets/vue-dc-comics-1/img/footer-bg.jpg);
    // DEBUG
    height: 300px;
}

.footer-social {
    background-color: #303030;
    // DEBUG
    height: 100px;
}
</style>
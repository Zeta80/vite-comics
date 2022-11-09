<script>

export default {
    name: "CardStructure",
    props: {
        thumb: String,
        series: String
    },


}
</script>

<template>
    <div class="card">
        <div class="img-cont">
            <img :src="thumb" :alt="series">
        </div>
        <h4>{{ series }}</h4>
    </div>
</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 10px);
    margin: 5px;

    .img-cont {
        width: 100%;
    }

    h4 {
        text-align: center;
        padding: .5rem;
    }

}
</style>
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
    text-align: start;

    .img-cont {
        width: 100%;
        height: 167px;
        overflow: hidden;
    }

    h4 {
        padding: .5rem;
    }

}
</style>
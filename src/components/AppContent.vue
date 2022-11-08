<script>
export default {
    name: "AppContent",
    data() {
        return {}
    }
}
</script>


<template>
    <div>
        <h2> -- > CONTENT HERE &lt-- </h2>
    </div>
</template>



<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

div {
    height: 500px;
    width: $container-size;
    margin: 0 auto;

    h2 {
        color: rgb(63, 186, 38);
    }
}
</style>
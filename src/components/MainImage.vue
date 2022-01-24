<template>
    <li class="col-4">
        <img :src="img" :alt="alt">
    </li>
</template>

<script>
export default {
    name: "MainImage",
    props: ["img", "alt"],
    data() {
        return {

        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_commons.scss";
li {
    display: block;
    margin-bottom: 2em;
    img {
        width: 100%;
    }
}
</style>
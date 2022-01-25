<template>
    <li class="col-4">
        <div class="box-image">
            <img :src="img" :alt="alt">
        </div>
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
@import "../assets/scss/partials/_main.scss";
li {
    display: block;
    margin-bottom: 2em;
    position: relative;
    @include box-img;
}
</style>
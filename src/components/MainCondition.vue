<template>
    <li class="col-3">
        <h4>{{ title }}</h4>
        <img :src="img" :alt="alt">
        <p>{{ text }}</p>
        <i class="fas fa-heart"></i>
        <i class="bi bi-123"></i>
    </li>
</template>

<script>
export default {
    name: "MainCondition",
    props: ["icons", "title", "img", "alt", "text"],
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
    text-align: center;
    i {
        color: red;
    }
    h4 {
        font-size: 1em;
        color: white;
        font-weight: 700;
    }
    p {
        color: $TextColorSummary;
    }
}
</style>
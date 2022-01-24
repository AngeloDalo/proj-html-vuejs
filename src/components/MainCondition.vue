<template>
    <li class="col-3 d-flex flex-column align-items-center">
        <div><i class="icons" :class="icons"></i></div>
        <h4>{{ title }}</h4>
        <img :src="img" :alt="alt">
        <p>{{ text }}</p>
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
    div {
        margin-bottom: 1em;
        border:1px solid red;
        border-radius: 100%;
        width: 50px;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        .icons {
            color: red;
            font-size: 1.5em;
        }
    }
    text-align: center;
    h4 {
        margin-bottom: 1em;
        font-size: 1em;
        color: white;
        font-weight: 700;
    }
    p {
        margin-top: 1em;
        color: $TextColorSummary;
    }
}
i {
    font-size: 2em;
}
</style>
<template>
    <li class="d-flex text-start">
        <div class="resultImg">
            <img :src="img" :alt="alt">
        </div>
        <div class="resultText ms-3">
            <p>{{ text }}</p>
            <span>{{ name }}</span>
        </div>
    </li>
</template>

<script>
export default {
    name: "MainResult",
    props: ["img", "alt", "text", "name"],
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
    width: 47.9%;
    padding: 1em;
    background-color: $ContainerSignUP;
    margin-bottom: 3em;
    margin-right: 0.8em;
    .resultImg {
        width: 30%;
        img {
            width: 100%;
        }
    }
    .resultText {
        width: 70%;
        p {
            color: #aaa9a9;
            font-family: italic;
        }
        span {
            color: #aaa9a9;
            font-weight: bold;
        }
    }
}
</style>
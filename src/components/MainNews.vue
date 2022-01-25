<template>
    <li class="col-4">
        <div class="box-img">
            <img :src="img" :alt="alt">
        </div>
        <div class="box-text">
            <h4>{{ name }}</h4>
            <p> {{ text }}</p>          
        </div>
    </li>
</template>

<script>
export default {
    name: "MainNews",
    props: ["img", "alt", "name", "text"],
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
    &:last-child {
        margin-top: -4em;
    }
    &:nth-child(4) {
        margin-top: -8em;
    }
    margin-bottom: 2em;
    .box-img {
        width: 100%;
        img {
            width: 100%;
        }
    }
    .box-text {
        background-color: $ContainerSignUP;
        padding: 1em;
        display: flex;
        flex-direction: column;
        h4 {
            color: white;
            font-weight: 700;
            text-align: start;
            width: 60%;
            font-size: 1.2em;
        }
        p {
            margin-top: 1em;
            margin-right: 1em;
            color: $TextColorSummary;
            text-align: start !important;
        }
        .box-icon {
            text-align: start;
            a {
                display: inline-block;
                padding: 0.5em;
                margin-right: 1em;
                background-color: $ContainerSignUP;
                .icons {
                    color: white;
                    font-size: 1.5em;
                    cursor: pointer;
                }
            }
        }
    }    
}
</style>
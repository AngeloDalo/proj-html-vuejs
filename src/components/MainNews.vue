<template>
    <li class="col-4">
        <div class="box-img">
            <img :src="img" :alt="alt">
            <div class="box-icons">
                <i class="icons fas fa-link"></i>
                <i class="icons fas fa-search"></i>
            </div>
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
@import "../assets/scss/partials/_main.scss";
li {
    &:last-child {
        margin-top: -4em;
    }
    &:nth-child(4) {
        margin-top: -8em;
    }
    margin-bottom: 2em;
    .box-img {
        position: relative;
        width: 100%;
        img {
            width: 100%;
        }
        .box-icons {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            display: none;
            .icons {
                margin-left: 0.3em;
                margin-right: 0.3em;
                font-size: 2em;
                color: white;
            }
        }
    }
    .box-img {
        transition: background-color 0.5s;
        &:hover img {
            opacity: 15%;
        }
        &:hover {
            background-color: #ea5f58;
        }
        &:hover {
            .box-icons {
                display: block;
            }
        }
    }
    @include box-text; 
}
</style>
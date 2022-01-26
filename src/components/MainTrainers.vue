<template>
    <li class="col-4">
        <div class="box-image">
            <img :src="img" :alt="alt">
        </div>
        <div class="box-text">
            <h4>{{ name }}</h4>
            <p> {{ text }}</p>  
            <div class="box-icon">
                <a href="#"><i class="icons fab fa-facebook-f"></i></a>
                <a href="#"><i class="icons fab fa-twitter"></i></a>
                <a href="#"><i class="icons fab fa-instagram"></i></a>
            </div>          
        </div>
    </li>
</template>

<script>
export default {
    name: "MainTrainers",
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
    @include box-img;
    @include box-text;
    .box-text {
        background-color: $ColorCubeBlak;
    } 
}
</style>
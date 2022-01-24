<template>
    <main>
        <div class="container-summary" id="about-us">
            <h2>WORLD CLASS Fitness</h2>
            <img src="../assets/img/divider-xx-red.png" alt="xx-red">
            <p>At Avada Gym, everything we do from top to bottom is of the heighest quality to ensure we're equipped to help you reach your goals of a healthy and fit lifestyle</p>
        </div>
    </main>
</template>

<script>
export default {
    name: 'Main',
    data () {
        return {

        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_commons.scss";
main {
    padding-top: 7em;
    padding-bottom: 7em;
    text-align: center;
    background-color: $ColorCubeBlak;
    .container-summary {
        h2 {
            color: white;
        }
        img {
            margin-top: 2em;
            margin-bottom: 2em;
        }
        p {
            margin-left: 25%;
            margin-right: 25%;
            color: $TextColorSummary;
            font-size: 0.9em;
        }
    }
}
</style>
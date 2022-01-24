<template>
    <main class="container-fluid">
        <div class="container-summary" id="about-us">
            <h2>WORLD CLASS Fitness</h2>
            <img src="../assets/img/divider-xx-red.png" alt="xx-red">
            <p>At Avada Gym, everything we do from top to bottom is of the heighest quality to ensure we're equipped to help you reach your goals of a healthy and fit lifestyle</p>
        </div>
        <div class="container-singup">
            <div class="row">
                <div class="col-6 d-flex justify-content-end">
                    <img src="../assets/img/home_img-compressor.jpg" alt="home_img-compressor">
                </div>
                <div class="col-6">
                    <h3>Sign Up For A Free Training Session</h3>
                    <form>
                        <label for="Name">Name*</label> <br>
                        <input type="text" id="Name" name="Name"> <br>
                        <label for="Name">Email</label> <br>
                        <input type="email" id="Email" name="Email"> <br>
                        <input type="submit" value="START NOW!">
                    </form>
                </div>
            </div>
        </div>
        <div class="container-condition">
            <ul class="row">
                <MainCondition
                    v-for="(cardCondition, index) in cardsCondition"
                    :key="index"
                    :icons = "cardCondition.icon"
                    :title = "cardCondition.title"
                    :img = "cardCondition.cross"
                    :alt = "cardCondition.title"
                    :text = "cardCondition.text" 
                />
            </ul>
        </div>
        <div class="container-results">
            <h2>real world results</h2>
            <img src="../assets/img/divider-xx-red.png" alt="xx-red">
                <ul class="row">
                    <MainResult
                        v-for="(resultCard, index) in resultCards"
                        :key="index"
                        :img = "resultCard.img"
                        :alt = "resultCard.name"
                        :text = "resultCard.text"
                        :name = "resultCard.name" 
                    />
            </ul>
        </div>
    </main>
</template>

<script>
import MainCondition from "./MainCondition.vue"
import MainResult from "./MainResult.vue"
export default {
    name: 'Main',
    components: {
        MainCondition,
        MainResult,
    },
    data () {
        return {
            cardsCondition: [
                {
                    "icon": "fas fa-unlink",
                    "title": "Srength & Conditioning",
                    "cross": require("../assets/img/divider-x-red.png"),
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisi, ordnare es volutpat etra us"
                },                {
                    "icon": "fas fa-bicycle",
                    "title": "Fitness & Cardio",
                    "cross": require("../assets/img/divider-x-red.png"),
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisi, ordnare es volutpat etra us"
                },                {
                    "icon": "fas fa-cloud",
                    "title": "Flexibility & Rest",
                    "cross": require("../assets/img/divider-x-red.png"),
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisi, ordnare es volutpat etra us"
                },                {
                    "icon": "fas fa-heartbeat",
                    "title": "Health & Diet",
                    "cross": require("../assets/img/divider-x-red.png"),
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisi, ordnare es volutpat etra us"
                },
            ],
            resultCards: [
                {
                    "img": require("../assets/img/review_1-compressor.jpg"),
                    "text": "“The trainers at Avada Gym have helped me reach my fitness goals beyond anything I could of hoped for. I love it!”",
                    "name": "– Tara Smith"
                },                {
                    "img": require("../assets/img/review_2-compressor.jpg"),
                    "text": "“The atmosphere at Avada Gym is amazing, the people are even better. All in all, it is a great place to work out.”",
                    "name": "– Simon Chel"
                },                {
                    "img": require("../assets/img/review_3-compressor-2.jpg"),
                    "text": "“The facilities at Avada Gym stood out to me the most. They are well maintained and have high quality equipment.”",
                    "name": "– Jen Wirth"
                },                {
                    "img": require("../assets/img/review_4-compressor-2.jpg"),
                    "text": "“No bad things to say about Avada Gym, they are top notch at every corner and truly take care of their customers.”",
                    "name": "– Jeff Glum"
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_commons.scss";
main {
    .container-summary {
        width: 100%;
        text-align: center;
        padding-top: 6em;
        padding-bottom: 6em;
        background-color: $ColorCubeBlak;
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
    .container-singup {
        width: 100%;
        background-color: $ContainerSignUP;
        .row {
            width: 75%;
            padding-top: 5em;
            padding-bottom: 5em;
            .col-6 {
                img {
                    width: 100%;
                    height: 250px;
                }
                h3 {
                    color:white;
                    font-size: 1.3em;
                    font-weight: bold;
                    margin-bottom: 2em;
                }
                form {
                    label {
                        color: $TextColorSummary;
                        margin-bottom: 0.5em;
                    }
                    input {
                        color: white;
                        width: 100%;
                        background-color: transparent;
                        border: 0.5px solid $TextColorSummary;
                    }
                    input:last-child {
                        color: white;
                        margin-top: 2em;
                        padding: 0.7em;
                        background-color: $SignUpButton;
                        border: none;
                    }
                }
            }
        }
    }
    .container-condition {
        background-image: url(../assets/img/gym_bkgd_bw-compressor.jpg);
        background-position: center;
        background-size: contain;
        padding-top: 5em;
        padding-bottom: 7em;
        width: 100%;
        .row {
            width: 75%;
        }
    }
    .container-results {
        text-align: center;
        width: 100%;
        background-color: $ColorCubeBlak;
        padding-top: 5em;
        padding-bottom: 7em;
        h2 {
            text-transform: uppercase;
            color: white;
        }
        .row {
            width: 75%;
        }
    }
}
</style>
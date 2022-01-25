<template>
    <main class="container-fluid">
        <div class="container-summary">
            <h2>WORLD CLASS Fitness</h2>
            <img src="../assets/img/divider-xx-red.png" alt="xx-red">
            <p>At Avada Gym, everything we do from top to bottom is of the heighest quality to ensure we're equipped to help you reach your goals of a healthy and fit lifestyle</p>
            <div class="square-summary"></div>
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
                    :key="index+cardsCondition.title"
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
                        :key="index+resultCard.name"
                        :img = "resultCard.img"
                        :alt = "resultCard.name"
                        :text = "resultCard.text"
                        :name = "resultCard.name" 
                    />
                </ul>
        </div>

        <div class="container-image">
            <h2>high performance facilities</h2>
            <img src="../assets/img/divider-xx-red.png" alt="xx-red">
                <ul class="row">
                    <MainImage
                        v-for="(imagesCard, index) in imagesCards"
                        :key="index+imagesCard.img"
                        :img = "imagesCard.img" 
                        :alt = "imagesCard.name"
                    />
                </ul>
        </div>

        <div class="container-phrase">
            <p>
                “ I fear not the man who has practiced 10,000 kicks once, but I fear the man who has practiced one kick 10,000 times ”
            </p>
            <span>BRUCE LEE • QUOTE OF THE DAY</span>
        </div>

        <div class="container-trainers">
            <h2>meet our trainers</h2>
            <img src="../assets/img/divider-xx-red.png" alt="xx-red">
                <ul class="row">
                    <MainTrainers
                        v-for="(trainersCard, index) in trainersCards"
                        :key="index+trainersCard.text"
                        :img = "trainersCard.img"
                        :alt = "trainersCard.alt"
                        :name = "trainersCard.name"
                        :text = "trainersCard.text"
                    />
                </ul>
            <button>view all trainers</button>
            <div class="square-trainers"></div>
        </div>

        <div class="container-news">
            <h2>performance news</h2>
            <img src="../assets/img/divider-xx-red.png" alt="xx-red">
                <ul class="row">
                    <MainNews
                        v-for="(newsCard, index) in newsCards"
                        :key="index"
                        :img = "newsCard.img"
                        :alt = "newsCard.alt"
                        :name = "newsCard.name"
                        :text = "newsCard.text"
                    />
                </ul>
            <button>read all articles</button>
        </div>
    </main>
</template>

<script>
import MainCondition from "./MainCondition.vue"
import MainResult from "./MainResult.vue"
import MainImage from "./MainImage.vue"
import MainTrainers from "./MainTrainers.vue"
import MainNews from "./MainNews.vue"
export default {
    name: 'Main',
    components: {
        MainCondition,
        MainResult,
        MainImage,
        MainTrainers,
        MainNews
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
            imagesCards: [
                {
                    "img": require("../assets/img/home-image1.jpg"),
                    "name": "img1"
                },                {
                    "img": require("../assets/img/home-image2.jpg"),
                    "name": "img2"
                },                {
                    "img": require("../assets/img/home-image3.jpg"),
                    "name": "img3"
                },                {
                    "img": require("../assets/img/home-image4.jpg"),
                    "name": "img4"
                },
                {
                    "img": require("../assets/img/home-image54.jpg"),
                    "name": "img5"
                },                {
                    "img": require("../assets/img/home-image6.jpg"),
                    "name": "img6"
                }, 
            ],
            trainersCards: [
                {
                    "img": require("../assets/img/trainer1.jpg"),
                    "alt": "Ann Baker Personal Trainer",
                    "name": "Ann Baker Personal Traine",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat."
                },                {
                    "img": require("../assets/img/trainer3.jpg"),
                    "alt": "Anne Warren Personal Trainer",
                    "name": "Anne Warren Personal Traine",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat."
                },                {
                    "img": require("../assets/img/trainer4.jpg"),
                    "alt": "Peter Rice Personal Trainer",
                    "name": "Peter Rice Personal Traine",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In augue nisl, onare volutpat."
                },
            ],
            newsCards: [
                {
                    "img": require("../assets/img/blog1.jpg"),
                    "alt": "blog1",
                    "name": "Train with free weights or your body weight?",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]"
                },                {
                    "img": require("../assets/img/blog6.jpg"),
                    "alt": "blog6",
                    "name": "Nutritional advice that will keep you training",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]"
                },                {
                    "img": require("../assets/img/trainer4.jpg"),
                    "alt": "trainer4",
                    "name": "Simple principles for your next workout",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]."
                },                {
                    "img": require("../assets/img/blog4.jpg"),
                    "alt": "blog4",
                    "name": "To be number one, train like you’re number two",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]"
                },                {
                    "img": require("../assets/img/trainer3.jpg"),
                    "alt": "trainer3",
                    "name": "Top 5 mistakes every gym member makes",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]"
                },                {
                    "img": require("../assets/img/trainer1.jpg"),
                    "alt": "trainer1",
                    "name": "The myths of shedding body fat explored",
                    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus. [...]."
                },                  
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_commons.scss";
@import "../assets/scss/partials/_main.scss";
main {
    .container-summary {
        position: relative;
        @include container-son;
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
        //tringolo fine pagina
        //quadrato di dimensioni fisse messo in absolute e ruotato di 45 gradi
        .square-summary {
            @include square;
            background-color: $ColorCubeBlak;
        }
    }
    .container-singup {
        @include container-son;
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
        @include container-son;
        background-image: url(../assets/img/gym_bkgd_bw-compressor.jpg);
        @include backgroud-image;
        padding-top: 5em;
        padding-bottom: 8em;
        .row {
            width: 75%;
        }
    }
    .container-results {
        @include container-son;
        @include padding-text;
        background-color: $ColorCubeBlak;
        h2 {
            text-transform: uppercase;
            color: white;
        }
        .row {
            width: 75%;
        }
    }
    .container-image {
        @include container-son;
        @include padding-text;
        background-color: $ColorCubeBlak;
        h2 {
            text-transform: uppercase;
            color: white;
        }
        .row {
            margin-top: 2em;
            width: 75%;
        }
    }
    .container-phrase {
        @include container-son;
        background-image: url(../assets/img/home-testimonial-bg.jpg);
        @include backgroud-image;
        text-align: center;
        padding: 7em 20em 10em 20em;
        color: white;
        p {
            font-size: 2em;
            margin-bottom: 3em;
        }
        span {
            font-weight: 700;
            text-transform: uppercase;
        }
    }
    .container-trainers {
        @include container-son;
        @include padding-text;
        position: relative;
        background-color: $ContainerSignUP;
        h2 {
            text-transform: uppercase;
            color: white;
        }
        .row {
            margin-top: 2em;
            width: 75%;
        }   
        button {
            background-color: transparent;
            border: 1px solid $TextColorSummary;
            color: $TextColorSummary;
            text-transform: uppercase;
            margin-top: 3em;
            padding: 0.5em 2em;
            &:hover {
                background-color: $TextColorSummary;
                color: black;
            }
        }  
        .square-trainers {
            background-color: $ContainerSignUP;
            @include square;
        }   
    }
    .container-news {
        @include container-son;
        @include padding-text;
        background-color: $ColorCubeBlak;
        h2 {
            text-transform: uppercase;
            color: white;
        }
        .row {
            margin-top: 2em;
            width: 75%;
        }  
        button {
            background-color: transparent;
            border: 1px solid $TextColorSummary;
            color: $TextColorSummary;
            text-transform: uppercase;
            margin-top: 3em;
            padding: 0.5em 2em;
            &:hover {
                background-color: $TextColorSummary;
                color: black;
            }
        } 
    }
}
</style>
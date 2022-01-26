<template>
    <header class="pt-3 ps-5">
        <div class="row">
            <!--logo sito-->
            <div class="col-6">
                <img src="..\assets\img\gym_logo_1x.png" alt="gym_logo_1x">
            </div>
            <!--link sito-->
            <div class="col-6">
                <ul class="d-flex justify-content-end align-items-center flex-wrap">
                    <li class="me-4" v-for="(linkHeader, index) in linksHeader" :key="index">
                        <a :href= linkHeader.link > {{ linkHeader.name }}</a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="jubotron">
            <h1>no pain no gain</h1>
            <p>Motivation is what gets your started. Habit is what keeps you going</p>
            <button>join us today</button>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data () {
        return {
        //link momentaneamente #, cambiarlo con link nel main una volta creato
        linksHeader: [
            {
                "name": "HOME",
                "link": "#" 
            },            {
                "name": "ABOUT US",
                "link": "#about-us" 
            },            {
                "name": "FACILITIES",
                "link": "#facilities" 
            },            {
                "name": "MEMBERSHIP",
                "link": "#membership" 
            },            {
                "name": "TESTIMONIALS",
                "link": "#testimonials" 
            },            {
                "name": "BLOG",
                "link": "#blog" 
            },
        ],
        }
    },
    created() {

    },
    methods: {

    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_commons.scss";
header {
    background-image: url(../assets/img/home-banner.jpg);
    background-position-x: center;
    background-size:cover;
    background-position-y: initial; 
    background-color: black;
    .row {
        .col-6 {
            img {
                width: 180px;
            }
            ul {
                height: 100%;
                li {
                    a {
                        color: white;
                    }
                    &:hover a {
                        color: red;
                    }
                }
            }
        }
    }
    .jubotron {
        padding-top: 16em;
        padding-bottom: 6.5em;
        text-align: center;
        h1 {
            font-size: 5em;
            font-weight: 700;
            color: white;
            text-transform: uppercase;
        }
        p {
            color: white;
        }
        button {
            background-color: transparent;
            border: 1px solid white;
            color: white;
            text-transform: uppercase;
            padding: 0.5em 1.3em;
            &:hover {
                background-color: white;
                font-weight: bold;
                color: black
            }
        }
    }
}
</style>
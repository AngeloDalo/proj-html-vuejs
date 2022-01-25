<template>
    <footer class="container-fluid">
        <div class="container-join row">
            <div class="box-text col-8">
                <h5>Achieve Your Fitness Goals</h5>
                <p>Flexible membership packages to suit all levels of athlete and achive your fitness goals</p>
            </div>
            <div class="box-button col-4">
                <button>join us</button>
            </div>
        </div>
        <div class="container-link row">
            <div class="col-3">
                <ul>
                    <li>COME FIND US</li>
                    <li>12345 North Main Street</li>
                    <li> New York, NY 555555</li>
                    <li>Phone: 1.800.555.6789</li>
                    <li>Phone: 1.800.555.6789</li>
                    <li><a href="#">Email: info@your-domain.com</a></li>
                </ul>
            </div>
            <div class="col-3">
                <ul>
                    <li>RECENT POSTS</li>
                    <li class="d-flex"><i class="fas fa-chevron-right me-1 mt-1"></i>Train with free weights or your body weight?</li>
                    <hr>
                    <li class="d-flex"><i class="fas fa-chevron-right me-1 mt-1"></i>Nutritional advice that will keep you training</li>
                </ul>
            </div>
            <div class="col-3">
                <ul>
                    <li>OPENING TIMES</li>
                    <li>Weekdays Monday – Friday<span> 09:00 – 19:00</span></li>
                    <li>Weekends Saturday – Sunday<span> 09:00 – 21:00</span></li>
                </ul>
            </div>
            <div class="col-3">
                <img src="../assets/img/gym_ad-compressor.jpg" alt="gym ad-compressor">
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data () {
        return {

        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/_variables.scss";
@import "../assets/scss/partials/_commons.scss";
.container-join {
    padding: 2em 15%;
    background-image: url(../assets/img/home-parallax.jpg);
    background-position: center;
    background-size: cover;
    .box-text {
        h5 {
            color: white;
            font-weight: 700;
            font-size: 1.5em;
        }
        p {
            font-size: 00.8em;
            color: white;
        }
    }
    .box-button {
        button {
            margin-top: 0.3em;
            background-color: transparent;
            border: 1px solid $TextColorSummary;
            color: $TextColorSummary;
            padding: 0.5em 1.5em;
            text-transform: uppercase;
            &:hover {
                background-color: $TextColorSummary;
                color: black;
            }
        }
    }
}
.container-link{
    background-color: $ContainerSignUP;
    padding: 2em 12.5%;
    ul {
        li:first-child {
            color: $ColorCubeGreyHard;
            margin-bottom: 1em;
        }
        li {
            color: $TextColorSummary;
            font-size: 0.9em;
            a {
                color: $TextColorSummary;
            }
            span {
                color: $ColorCubeGreyHard;
            }
        }
        hr {
            color: $ColorCubeGreyHard;
        }
    }
    img {
        width: 90%;
    }
}
</style>
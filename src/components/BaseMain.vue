<template>
    <main>
        <div id="background">
            <span id="current-series">CURRENT SERIES</span>
        </div>
        <div class="container box">
            <ComicCard v-for="comic in Comics" :key="comic['thumb']" :comic="comic"/>
        </div>
    </main>
</template>

<script>
import ComicCard from './ComicCard.vue'

export default {
    name: 'BaseMain',
    components: {
    ComicCard,
},
    props: {
        Comics: Array,
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/sass/vars';

    main {
        background-color: #1C1C1C;

        #background{
            height: 400px;
            background-image: url(../assets/img/jumbotron.jpg);
            background-position: top;
            position: relative;

            #current-series {
                font-size: 1.5rem;
                font-weight: bold;
                padding: 5px;
                background-color: $color_blue;
                position: absolute;
                bottom: -20px;
                left: 120px;
            }
        }

        .box {
            display:flex;
            flex-wrap: wrap;
            justify-content: space-around;
            padding-top: 50px;
        }
    }
</style>


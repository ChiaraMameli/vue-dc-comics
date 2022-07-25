<template>
    <main>
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
    main {
        background-color: #1C1C1C;

        .box {
            display:flex;
            flex-wrap: wrap;
            justify-content: space-around;
            padding-top: 50px;
        }
    }
</style>


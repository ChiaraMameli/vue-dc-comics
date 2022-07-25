<template>
    <div  class="comic-card">
        <figure>
            <img :src="comic['thumb']" :alt="comic['series']">
        </figure>
        <figcaption>{{comic['series']}}</figcaption>
    </div>
</template>

<script>
export default {
    name: 'ComicCard',
    props: {
        comic: Object,
    }
}
</script>

<style lang="scss" scoped>
    .comic-card{
    flex-basis: calc((100% / 6) - 20px);
    padding-bottom: 50px;


    img{
        height: 200px;
        width: 200px;
        object-fit: cover;
        object-position: 0% 0%;
    }

    figcaption{
        text-transform: capitalize;
    }
    }

</style>
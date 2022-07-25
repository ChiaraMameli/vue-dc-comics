<template>
  <section id="bonus-section">
    <div class="container">
        <figure v-for="link in BonusLinks" v-bind:key="link.img">
            <img :src="link.src" :alt="link.text">
            <figcaption><a :href="link.ref">{{link.text}}</a></figcaption>
        </figure>
    </div>
  </section>
</template>

<script>
export default {
    name: 'BonusSection',
    props: {
        BonusLinks: Array,
    }

}
</script>

<style lang="scss" scoped>

@import '../assets/sass/vars';

    #bonus-section {
        background-color: $color_blue;
        padding: 2rem 0;

        .container {
        display: flex;
        flex-wrap: nowrap;
        justify-content: space-between;
        }

        figure {
        display: flex;
            img{
            width: 2rem;
            object-fit: contain;
            }
            figcaption{
            align-self: center;
            margin-left: 1rem;
            text-transform: capitalize;
                a {
                color: #FFF;
                }
            }
        }
    }
</style>
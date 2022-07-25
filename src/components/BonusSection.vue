<template>
  <section id="bonus-section">
    <div class="container">
        <figure v-for="link in links" v-bind:key="link.img">
            <img :src="link.img" :alt="link.text">
            <figcaption><a :href="link.url">{{link.text}}</a></figcaption>
        </figure>
    </div>
  </section>
</template>

<script>
export default {
    name: 'BonusSection',
    data(){
    return{
        links: [
            {
                img: require("../assets/img/buy-comics-digital-comics.png"),
                url: '#',
                text: 'Digital Comics',
            },
            {
                img: require("../assets/img/buy-comics-merchandise.png"),
                url: '#',
                text: 'DC Merchandise',
            },
            {
                img: require("../assets/img/buy-comics-subscriptions.png"),
                url: '#',
                text: 'Subscription',
            },
            {
                img: require("../assets/img/buy-comics-shop-locator.png"),
                url: '#',
                text: 'Comic Shop Locator',
            },
            {
                img: require("../assets/img/buy-dc-power-visa.svg"),
                url: '#',
                text: 'DC Powe Visa',
            },
        ]
    }}
}
</script>

<style lang="scss" scoped>

//  @import '../assets/sass/vars';

    #bonus-section {
        background-color: #1E82F6;
        padding: 2rem 0;

        .container {
        display: flex;
        flex-wrap: nowrap;
        justify-content: space-between;
        }

        figure {
        display: flex;
            img{
            max-width: 2.5rem;
            }
            figcaption{
            align-self: center;
            margin-left: 1rem;
                a {
                color: #FFF;
                }
            }
        }
    }
</style>
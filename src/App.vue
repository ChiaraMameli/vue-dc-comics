<template>
  <div>
    <BaseHeader :header-links= "HeaderLinks"/>
    <BaseMain />
    <BonusSection :bonus-links="BonusLinks" />
    <BaseFooter />
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue'
import BaseMain from './components/BaseMain.vue'
import BaseFooter from './components/BaseFooter.vue'
import BonusSection from './components/BonusSection.vue'

export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseMain,
    BaseFooter,
    BonusSection
},
data(){
  return {
      HeaderLinks: [
          {
            text: 'Characters',
            url: '#',
            current: false,
          },
          {
            text: 'Comics',
            url: '#',
            current: true,
          },
          {
            text: 'Movies',
            url: '#',
            current: false,
          },
          {
            text: 'TV',
            url: '#',
            current: false,
          },
          {
            text: 'Games',
            url: '#',
            current: false,
          },
          {
            text: 'Collectibles',
            url: '#',
            current: false,
          },
          {
            text: 'Videos',
            url: '#',
            current: false,
          },
          {
            text: 'Fans',
            url: '#',
            current: false,
          },
          {
            text: 'News',
            url: '#',
            current: false,
          },
          {
            text: 'Shop',
            url: '#',
            current: false,
          },
             ],
      BonusLinks: [
        {
            src: require("./assets/img/buy-comics-digital-comics.png"),
            ref: '#',
            text: 'Digital Comics',
        },
        {
            src: require("./assets/img/buy-comics-merchandise.png"),
            ref: '#',
            text: 'DC Merchandise',
        },
        {
            src: require("./assets/img/buy-comics-subscriptions.png"),
            ref: '#',
            text: 'Subscription',
        },
        {
            src: require("./assets/img/buy-comics-shop-locator.png"),
            ref: '#',
            text: 'Comic Shop Locator',
        },
        {
            src: require("./assets/img/buy-dc-power-visa.svg"),
            ref: '#',
            text: 'DC Powe Visa',
        },
    ]

  }
}
}
</script>

<style lang="scss">
@import './assets/sass/style.scss';
</style>

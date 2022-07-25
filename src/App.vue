<template>
  <div>
    <BaseHeader :header-links= "HeaderLinks"/>
    <BaseMain />
    <BonusSection />
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
             ]
  }
}
}
</script>

<style lang="scss">
@import './assets/sass/style.scss';
</style>

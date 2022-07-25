<template>
  <div>
    <BaseHeader />
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
}
}
</script>

<style lang="scss">
@import './assets/sass/style.scss';
</style>

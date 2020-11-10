<template lang="pug">
  #app
    TheHeader
    Headliner
    EnquireNowSection
    LearnMoreSection
    TheFooter
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/_shared/TheHeader.vue'
import TheFooter from './components/_shared/TheFooter.vue'
import Headliner from './components/landing/Headliner.vue'
import EnquireNowSection from './components/landing/enquire-now/EnquireNowSection.vue'
import LearnMoreSection from './components/landing/LearnMoreSection.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader,
    TheFooter,
    Headliner,
    EnquireNowSection,
    LearnMoreSection
  }
}
</script>

<style lang="scss" scoped>
@import './assets/styles/_variables.scss';
@import './assets/styles/_helpers.scss';

#app {
  font-family: "Helvetica New", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $primary-text;
  height: 100%;
}
</style>

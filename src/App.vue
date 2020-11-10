<template lang="pug">
  #app
    TheHeader
    Headliner
    EnquireNowSection
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/_shared/TheHeader.vue'
import Headliner from './components/landing/Headliner.vue'
import EnquireNowSection from './components/landing/enquire-now/EnquireNowSection.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader,
    Headliner,
    EnquireNowSection
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

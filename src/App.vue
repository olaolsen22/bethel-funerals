<template lang="pug">
  #app
    TheHeader
    Headliner
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/_shared/TheHeader.vue'
import Headliner from './components/landing/Headliner.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader,
    Headliner
  }
}
</script>

<style>
#app {
  font-family: "Helvetica New", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>

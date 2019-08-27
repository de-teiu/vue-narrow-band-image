<template>
  <div id="app">
    <narrow-band-image src="/sample.jpg"/>
  </div>
</template>

<script>
import NarrowBandImage from './components/NarrowBandImage.vue'

export default {
  name: 'app',
  components: {
    NarrowBandImage
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

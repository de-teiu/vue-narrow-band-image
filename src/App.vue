<template>
  <div id="app">
    <h1>Vue-Narrow-Band-Image</h1>
    <narrow-band-image src="/sample.jpg"/>
    <h3>いかがでしたか？</h3>
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
  margin-top: 20px;
}
</style>

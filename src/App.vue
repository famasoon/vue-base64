<template>
  <div id="app">
    <Encoder />
  </div>
</template>

<script>
import Encoder from './components/Encoder.vue'

export default {
  name: 'app',
  components: {
    Encoder,
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

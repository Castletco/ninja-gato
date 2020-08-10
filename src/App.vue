<template>
  <div id="app">
    <NinjaGato />
  </div>
</template>

<script>
import NinjaGato from './components/NinjaGato.vue'

export default {
  name: 'App',
  components: {
    NinjaGato
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

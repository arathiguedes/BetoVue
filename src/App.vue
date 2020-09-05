<template>
  <div id="app">
    <!-- <img alt="Beto" src="./assets/beto.png"> -->
    <Meet msg="Esse é o meet escrito no app.vue"/>
  </div>
</template>

<script>
import Meet from './components/Meet.vue'

export default {
  name: 'App',
  components: {
    Meet
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

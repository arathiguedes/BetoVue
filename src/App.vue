<template>
  <div id="app">
<<<<<<< HEAD
    <!-- <img alt="Beto" src="./assets/beto.png"> -->
    <Meet msg="Esse é o meet escrito no app.vue"/>
=======
    <img alt="Beto" src="./assets/beto.png">
    <HelloWorld msg="Welcome to BetoVue.js App"/>
    <Card/>
>>>>>>> 2182c8f... instal ionic
  </div>
</template>

<script>
<<<<<<< HEAD
import Meet from './components/Meet.vue'

export default {
  name: 'App',
  components: {
    Meet
=======
import HelloWorld from './components/HelloWorld.vue'
import Card from './components/Card.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Card
>>>>>>> 2182c8f... instal ionic
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

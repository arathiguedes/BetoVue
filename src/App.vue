<template>
  <div id="app">
    <img alt="Beto" src="./assets/beto.png">
    <HelloWorld/>
    <Chat/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Chat from './components/Chat.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Chat
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

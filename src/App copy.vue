<template>
  <div id="app">
    <img alt="Beto" src="./assets/beto.png">
    <HelloWorld msg="Welcome to BetoVue.js App"/>
    <button @click="jitsi()">cria o meet</button>
    <div id="meet"></div>
  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
   components: {
     HelloWorld
   },
  methods:{
    jitsi(){
      let domain = 'meet.jit.si';
      let options = {
        roomName: 'testroom',
        width: 500,
        height: 500,
        interfaceConfigOverwrite: { filmStripOnly: false },
        parentNode: document.querySelector('#meet')
      };
      new window.JitsiMeetExternalAPI(domain, options);

    },
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

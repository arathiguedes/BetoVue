<template>
  <div id="app">
    <!-- <img alt="Beto" src="./assets/beto.png"> -->
    <Meet/>
    <div id="box" style="display: none">
      <Chat/>
    </div>
  </div>
</template>

<script>
import Chat from './components/Chat.vue'

export default {
  name: 'App',
  components: {
    Meet,
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
  position:absolute;
  width: 99%;
  /* height: 100%; */
  top:0;
}
#box {
 background-color:rgba(22,38,55,1.0);
 /* background-color:rgba(183, 212, 19, 1.0); */
 box-sizing:border-box;
 color:#fff;
 flex-direction:column;
 height:100%;
 overflow:hidden;
 position:absolute;
 top:0;
 width:375px;
 /* display: none;  used inline because*/
 z-index:100
}
</style>

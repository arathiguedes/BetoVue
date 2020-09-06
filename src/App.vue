<template>
  <div id="app">
    <!-- <img alt="Beto" src="./assets/beto.png"> -->
    <Meet/>
    <div id="box"></div>
    <!-- <div>
      <button @click="jitsi()">cria o meet</button>
    </div> -->
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
  position:absolute;
  width: 99%;
  /* height: 100%; */
  top:0;
}
#box {
 /* background-color:rgba(22,38,55,.8); */
 background-color:rgba(183, 212, 19, 1.0);
 box-sizing:border-box;
 color:#fff;
 /* display:flex; */
 flex-direction:column;
 height:100%;
 overflow:hidden;
 position:absolute;
 top:0;
 width:375px;
 /* z-index:300 */
}
</style>

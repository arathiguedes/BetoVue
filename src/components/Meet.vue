<template>
  <div class="meet">
  <button @click="jitsi()">cria o meet</button>
  </div>
</template>

<script>
export default {
    name: 'Meet',
    props: {
        msg: String
  },
    methods:{
        jitsi(){
        let domain = 'meet.jit.si';
        let options = {
            roomName: 'testroom',
            width: 500,
            height: 500,
            interfaceConfigOverwrite: { filmStripOnly: false},
            parentNode: document.querySelector('#meet')
        };
        new window.JitsiMeetExternalAPI(domain, options);
        },
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

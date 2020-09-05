<template>
  <div class="app">
  <div id="meet"></div>
  <!-- <button @click="jitsi()">cria o meet</button> -->
  </div>
</template>

<script>
export default {
    name: 'Meet',
    props: {
        msg: String
  },
        mounted(){
        let domain = 'meet.jit.si';
        let options = {
            roomName: 'testroom',
            // width: 500,
            height: 500,
            interfaceConfigOverwrite: { filmStripOnly: false},
            parentNode: document.querySelector('#meet')
        };
        new window.JitsiMeetExternalAPI(domain, options);
        },
}
</script>

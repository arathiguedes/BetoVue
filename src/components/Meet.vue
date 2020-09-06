<template>
  <div class="app">
  <div id="meet" style="height: 100vh"></div>
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
            roomName: 'nomedaassembleia', // todo implementar forma de mudar o nome da assembleia
            width: '100%',
            height: '100%',
            interfaceConfigOverwrite: { filmStripOnly: false},
            parentNode: document.querySelector('#meet')
        };
        new window.JitsiMeetExternalAPI(domain, options);
        },
}
</script>

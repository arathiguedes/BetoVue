<template>
  <div class="app">
  <div id="meet" style="height: 99vh">
    <!-- <button @click="chat()">chat</button> -->
  </div>
  </div>
</template>

<script>
export default {
    name: 'Meet',
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
    // const api = new window.JitsiMeetExternalAPI(domain, options);
    },
    // methods:{
    //   chat(){
    //     api.executeCommand('toggleChat');
    //   }
    // },
}
</script>

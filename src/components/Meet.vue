<template>
  <div class="app">
  <div id="meet" style="height: 99vh">
    <div @click="chat()" id="boxbutton"><svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="8" y1="6" x2="21" y2="6"></line><line x1="8" y1="12" x2="21" y2="12"></line><line x1="8" y1="18" x2="21" y2="18"></line><line x1="3" y1="6" x2="3.01" y2="6"></line><line x1="3" y1="12" x2="3.01" y2="12"></line><line x1="3" y1="18" x2="3.01" y2="18"></line></svg></div>
  </div>
  </div>
</template>

<script>
let api;// = new window.JitsiMeetExternalAPI(domain, options);
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
    
    api = new window.JitsiMeetExternalAPI(domain, options);
    // const api = new window.JitsiMeetExternalAPI(domain, options);
    },
    methods:{
      chat(){
        const box = document.getElementById("box")
        console.log(box)
        console.log("ieaoi")
        if (box.style.display === "none") {
          box.style.display = "block";
        } 
        else {
          box.style.display = "none";
        }
        api.executeCommand('toggleChat');
      }
    },
}
</script>

<style scoped>
  #boxbutton {
    position: absolute;
    bottom: 20px;
    right: 180px;
    z-index: 10h0;
    /* <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="8" y1="6" x2="21" y2="6"></line><line x1="8" y1="12" x2="21" y2="12"></line><line x1="8" y1="18" x2="21" y2="18"></line><line x1="3" y1="6" x2="3.01" y2="6"></line><line x1="3" y1="12" x2="3.01" y2="12"></line><line x1="3" y1="18" x2="3.01" y2="18"></line></svg> */

  }

</style>
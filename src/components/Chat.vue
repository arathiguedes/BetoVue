<template>
    <div id="app">
        <button id="chat-beto" @click="Chamajanela()">icone</button>
        <span>{{EstadoJanela}}</span>
        <div id="janela" v-if="EstadoJanela" >
            <div class="bts">
            <button style="background-color: green;" @click="filtraEstado('green')"></button>
            <button style="background-color: red;" @click="filtraEstado('red')"></button>
            <button style="background-color: yellow;" @click="filtraEstado('yellow')"></button>
            <button style="background-color: grey;" @click="filtraEstado('grey')"></button>
            </div>
            <div id="card">
            <div v-for="card in cardsExibe" :key="card.tema">
                <div v-if="cards.length == 0">Sem cartas</div>
                {{card}}
            </div>
            
            </div>

            <div id="forms">

            <h3>Cadastre sua Palta</h3>
            <input type="text" placeholder="Tema" v-model="TemaField" > 
            <input type="text" placeholder="Descricao" v-model="DescField">
            <label for="pauta">Estado da pauta:</label>
            <select id="pauta "name="estado" v-model="estado">
                <option value="green">discutida</option>
                <option value="red">discutindo</option>
                <option value="yellow">Nova a discutir</option>
                <option value="grey">Futura a discutir</option>
            </select> 
            <button @click="CadastraPalta">CadastraPauta</button>
            
            </div>
        </div>
    </div>
</template>

<style scoped>
    #janela {
    position: relative;
    background-color: #ececec;
    height: 600px;
    width: 500px;
    }
    #card{
    padding: 20px 20px 20px 50px;
    max-height: 76%;
    overflow-x: hidden; 
    overflow-y: auto;
    max-width: 100%;  
    }
    #forms {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 10px;
    text-align: center;
    border-top: 2px solid white;
    max-width: 100%;
    max-height: 20%;
    }

    .bts{
    position: absolute;
    left: 10px;
    height: 76%;
    display: inline-flex;
    flex-direction: column;
    justify-content: space-around;
    }
    .bts button{
    width: 30px;
    height: 30px;
    border-radius: 50px;
    }

</style>

<script>
    export default{
        name: 'Chat',
        data() {
            return{
                TemaField: "",
                DescField: "",
                estado: "",
                EstadoJanela: false,
                cards: [
                    {
                        tema: "Pauta 1",
                        descricao: "sldkasjdlkasjdlasskldasjdklasdjasl",
                        estado: "green"
                        
                    },
                    {
                        tema: "Pauta 2",
                        descricao: "sldkasjdlkasjdlasskldasjdklasdjasl",
                        estado: "red"
                        
                    },
                    {
                        tema: "Pauta 3",
                        descricao: "sldkasjdlkasjdlasskldasjdklasdjasl",
                        estado: "yellow"
                        
                    },
                    {
                        tema: "Pauta 4",
                        descricao: "sldkasjdlkasjdlasskldasjdklasdjasl",
                        estado: "grey"
                        
                    },
                    {
                        tema: "Pauta 5",
                        descricao: "sldkasjdlkasjdlasskldasjdklasdjasl",
                        estado: "green"
                        
                    },
                    {
                        tema: "Pauta 6",
                        descricao: "sldkasjdlkasjdlasskldasjdklasdjasl",
                        estado: "red"
                        
                    },
                    {
                        tema: "Pauta 7",
                        descricao: "sldkasjdlkasjdlasskldasjdklasdjasl",
                        estado: "yellow"
                        
                    },
                    {
                        tema: "Pauta 8",
                        descricao: "sldkasjdlkasjdlasskldasjdklasdjasl",
                        estado: "grey"
                        
                    }
                ],
                cardsExibe: []
            }
        },

        methods: {
          CadastraPalta: function() { 
              this.cards.push({tema: this.TemaField,descricao: this.DescField, estado: this.estado})
              this.TemaField = ""
              this.DescField = ""

            },
          Chamajanela: function() {
            if (this.EstadoJanela === false){this.EstadoJanela = true} else {this.EstadoJanela = false}
            this.cardsExibe = this.cards
          },
          filtraEstado(cor) {
              console.log("filtraEstado",cor)
              this.cardsExibe = this.cards.filter(card => card.estado === cor)
          }
          }
      }
</script>
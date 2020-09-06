<template>
  <v-card
    class="mx-auto branco"
    max-width="344"
  >
    <v-card-text>
      <div>Pauta</div>
      <p class="display-1 text--primary">
        {{tema}}
      </p>
      <p>Descrição</p>
      <div class="text--primary">
        {{descricao}}
      </div>
    </v-card-text>
    <v-card-actions>
      <v-btn
        text
        color="deep-purple accent-4"
      >
        {{status}}
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
    name: 'Card',
    props: {
        tema: {
            type : String
        },
    
        descricao: {
            type : String
        },
        status: {
            type : String
        }
    }
}
</script>
    
<style>
    .branco{
        background-color: floralwhite;
        margin: 5px;
    }
</style>


<template lang="html">

  <button @click="disparaAcao()" :type="tipo"  :class="estiloDoBotao">{{ rotulo }}</button>

</template>

<script>
export default {

  props: {
       tipo: {
           type: String,
           required: true
       },

       rotulo: {
           type: String,
           required: true
       },

       confirmacao: Boolean,
       estilo: String
   },

  methods: {

    disparaAcao(){
      if (this.confirmacao) {
        if (confirm("Confirma ação?")) {
          this.$emit('botaoAtivado');
        }
        return;
      }
    }

  },

  computed: {
    estiloDoBotao() {
      if (this.estilo == 'padrao' || !this.estilo) {
        return 'botao botao-padrao'
      }
      if (this.estilo == 'perigo') {
        return 'botao botao-perigo'
      }
    }
  }

}
</script>

<style lang="css">

  .botao {
    display: inline-block;
    padding: 10px;
    border-radius: 3px;
    margin: 10px;
    font-size: 1.2em;
  }

  .botao-perigo {
    background: firebrick;
    color: white;
  }

  .botao-padrao {
    background: darkcyan;
    color: white;
  }

</style>

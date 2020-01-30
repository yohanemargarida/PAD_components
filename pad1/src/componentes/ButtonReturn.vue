<template>
  <div class="Detalhes">
    <h1>Detalhes</h1>
    <div class="button-return" id="app1">
      <button @click="irParaInicio" id="send">voltar</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    irParaInicio() {
      this.$router.push("/");
    }
  }
};
</script>
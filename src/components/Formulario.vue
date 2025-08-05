<template>
  <div>
    <h1 class="mb-3 text-center">Cadastro de estudantes</h1>
    <input type="text" class="form-control mb-5" placeholder="nome" v-model="estudante.nome"/>
    <input type="text" class="form-control mb-5" placeholder="curso" v-model="estudante.curso"/>
    <input type="text" class="form-control mb-5" placeholder="idade" v-model="estudante.idade"/>
    <input type="text" class="form-control" placeholder="periodo" v-model="estudante.periodo"/>
    <br /><br />
    <button class="btn btn-success mb-5" @click="cadastrarUsuario">Cadastrar</button>
  </div>
</template>
<script>

export default {
  data() {
    return {
      estudante: {
        nome: "",
        curso: "",
        idade: 0,
        periodo: 0,
      },
    };
  },
  methods: {
    
  },
};
</script>
<style></style>

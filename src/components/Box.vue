<template>
  <div>
    <div class="row">
      <div class="col box">
        <h6><strong>Nome:</strong> {{ nome }}</h6>
        <h6><strong>Idade:</strong> {{ idade }}</h6>
        <h6><strong>Curso:</strong> {{ curso }}</h6>
        <h6><strong>Periodo:</strong> {{ periodo }}</h6>

        <div class="d-flex justify-content-end gap-2 mt-3">
          <button
            class="btn btn-danger btn-sm"
            
            id="liveToastBtn"
          >
            Deletar
          </button>
          <button class="btn btn-warning btn-sm">Alterar</button>
        </div>
      </div>
    </div>
    <br />
  </div>
</template>
<script>

export default {
  props: ["propNome", "propIdade", "propCurso", "propPeriodo", "propId"],
  data() {
    return {
      id: this.propId,
      nome: this.propNome,
      idade: this.propIdade,
      curso: this.propCurso,
      periodo: this.propPeriodo,
    };
  },
  methods: {
  
  },
};
</script>
<style>
.box {
  width: 100%;
  height: auto; /* melhor que altura fixa */
  border: 2px solid rgb(201, 201, 201);
  border-radius: 25px;
  padding: 20px 35px;
  box-sizing: border-box;
  background-color: #f8fbff; /* opcional para destacar */
  margin-bottom: 20px; /* espaçamento entre caixas */
}
</style>

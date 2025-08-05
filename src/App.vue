<template>
  <div>
    <div v-if="flag">
      <h1 class="mb-5 text-center">Listagem dos Alunos</h1>
      <input type="text" class="form-control input-group-lg " >
      <div v-for="estudante in estudantes" :key="estudante.id">
        <box
      
         :propId="estudante.id"
          :propNome="estudante.nome"
          :propIdade="estudante.idade"
          :propCurso="estudante.curso"
          :propPeriodo="estudante.periodo"
        ></box>
        <!-- <div class="row">
          <div class="col-8"></div>
          <div class="col-4"></div>
        </div> -->
      </div>
    </div>
    <div v-else>
      <formulario></formulario>
    </div>

    <div class="row">
      <div class="col-8"></div>
      <div class="col-4 d-flex justify-content-end">
        <button class="btn btn-primary btn-lg" @click="flag = !flag">
          {{ mostrar }}
        </button>
      </div>
    </div>
  </div>
</template>
<script>
import box from "./components/Box.vue";
import Formulario from "./components/Formulario.vue";

export default {
  label: "",
  components: { box, Formulario },
  computed: {
    mostrar() {
      if (this.flag) {
        return "Cadastrar";
      } else {
        return "Visualizar";
      }
    },
  },
  mounted() {
    
  },
  methods: {
   
  },
  data() {
    return {
      flag: false,
      estudantes: [],
      propriedades: [
        {
          id: 1,
          nome: "Bia",
          idade: 33,
          curso: "Desenvolvedora Fullstack",
          periodo: "Manhã",
        },
        {
          id: 2,
          nome: "Tarcisio",
          idade: 40,
          curso: "Analista de dados",
          periodo: "Manhã",
        },
        { id: 3, nome: "Rayane", idade: 29, curso: "Tester", periodo: "Manhã" },
      ],
    };
  },
};
</script>
<style></style>

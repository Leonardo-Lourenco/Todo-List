<template>


  <div id="app">

    <div class="container grid-xs py-2">

      <img class="img-responsive" src="@/assets/task.png" alt="CoffeeTagTodo">

      <form @submit.prevent="addTarefa(tarefa)">

         
          <div class="input-group">

            <input type="text" v-model="tarefa.description" class="form-input"  placeholder=" Adicionar uma Tarefa">
            <button class="btn btn-success input-group-btn "><i class="icon icon-arrow-right"></i> Adicionar </button>

          </div>


          <ul class="step">
              <li class="step-item active">
                <a href="#" class="tooltip" data-tooltip="Step 1">Step 1</a>
                          </li>
              <li class="step-item">
                <a href="#" class="tooltip" data-tooltip="Step 2">Step 2</a>
                          </li>
              <li class="step-item">
                <a href="#" class="tooltip" data-tooltip="Step 3">Step 3</a>
              </li>
              <li class="step-item">
                <a href="#" class="tooltip" data-tooltip="Step 4">Step 4</a>
              </li>
            </ul>

            {{ tarefas }}

      </form>



    </div>



  </div>


</template>

<script>

  export default {


    name: 'App',

    data() {

      return { tarefas: [], tarefa:  { checked: false} };


    },

    methods: {

      addTarefa(tarefa) {
        
        tarefa.id = Date.now();
        this.tarefas.push(tarefa);


      }
    }


  
}



</script>

<style scoped>

    img {

      max-width: 150px;
      margin: 0 auto;

    }



</style>

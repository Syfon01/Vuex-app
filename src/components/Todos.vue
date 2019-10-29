<template>
  <div class="py-3">
    <h1 class="text-center">Todos</h1>
      <div class = "todos row">
        <div class= "todo col-md-3 col-sm-4 my-2"
           v-for="todo in allTodos" :key="todo.id">
            <div class ="card bg-success p-3 text-center text-white">
              {{todo.title}}
              <i class="fas fa-trash-alt" @click="deleteTodo(todo.id)"></i>
            </div>  
        </div>
      </div>
  </div>
</template>

<script>
  import {mapGetters, mapActions} from 'vuex';
  export default {
    name: 'Todos',
    methods:{
      ...mapActions(['fetchTodos', 'deleteTodo'])
    },
    computed:{
      ...mapGetters(['allTodos'])
    },
    created(){
      this.fetchTodos();
    }
  }
</script>

<style scoped>
i{
  position: absolute;
  bottom: 10px;
  right:10px;
  cursor:pointer;
}
.card{
  height: 100px;
}
</style>
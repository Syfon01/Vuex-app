<template>
  <div id="app" class="container bg-light p-5">
    <AddTodo/>
    <FilterTodo/>    
    <Todos/>
  </div>
</template>

<script>
import Todos from './components/Todos.vue'
import AddTodo from './components/AddTodo.vue'
import FilterTodo from './components/FilterTodo.vue'

export default {
  name: 'app',
  components: {
    Todos,
    AddTodo,
    FilterTodo,
  }
}
</script>

<style>

</style>

<template>
  <div>
  <h3>Add Todo</h3>
  <div class="container">
    <form @submit="OnSubmit">
          <input type="text" v-model="title"  placeholder="Add Todos..">
          <input name="" id="" class="btn-success" type="submit" value="submit">              
    </form>
  </div>
  </div>
</template>

<script>
import {mapActions} from 'vuex';
  export default {
    name: 'AddTodo',
  data(){
    return{
      title: ''
    }
  },
  methods:{
    ...mapActions(['addTodo']),
    OnSubmit(e){
      e.preventDefault();
      this.addTodo(this.title)
    }
  }
}
</script>

<style scoped>
form{
  display: flex;
}
input[type="text"]{
  flex: 10;
  padding: 10px;
}
input[type="submit"]{
  flex: 2;
  padding: 10px;
}
</style>
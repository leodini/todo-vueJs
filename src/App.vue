<template>
  <div id="app">
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Todos from './components/Todos'


export default {
  name: 'app',
  components: {
    Todos
  },
  data(){
    return {
      todos: [
        {
          id: 1,
          title: 'Todo one',
          completed: false
        },
        {
          id: 2,
          title: 'todo two',
          completed: false
        },
        {
          id: 3,
          title: 'todo three',
          completed: false
        }
      ]
    }
  },
  methods: {
    deleteTodo(id){
      this.todos = this.todos.filter(todo => todo.id !== id);
    }
  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box
  }

  body{
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
</style>

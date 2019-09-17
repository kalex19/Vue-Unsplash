<template>
  <div id="app">
    <Header/>
    <Form v-on:add-todo="addTodo" />
    <TodoContainer v-bind:todos="todos" v-on:del-todo="deleteTodo" v-on:line-through="lineThrough" v-on:star-todo="starTodo"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Form from './components/Form.vue'
import TodoContainer from './components/TodoContainer.vue'

export default {
  name: 'app',
  components: {
    Header,
    Form,
    TodoContainer
  }, 
  data() {
    return {
      todos: [
        {
          id: 1,
          text: "Cook Dinner",
          completed: false,
          starred: false
        },
        {
          id: 2,
          text: "Make Bed",
          completed: false,
          starred: false
        },
        {
          id: 3,
          text: "Water Plants",
          completed: false,
          starred: false
        }
      ]
    }
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter(todo => todo.id !== id)
    },
    lineThrough(id) { 
      const todoToggle = this.todos.find(todo => todo.id === id);
      todoToggle.completed = !todoToggle.completed
      this.$forceUpdate()
    },
    addTodo(newTodo){
      this.todos = [...this.todos, newTodo]
    },
    starTodo(id){
      const todoToggle = this.todos.find(todo => todo.id === id);
      todoToggle.starred = !todoToggle.starred
      this.$forceUpdate()
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-image: url('./assets/lauren-sauder-6GPBVYLapYQ-unsplash.jpg');
  background-repeat: no-repeat;
}
</style>

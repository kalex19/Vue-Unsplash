<template>
  <div id="app">
    <Form v-on:add-todo="addTodo" />
    <ImageContainer v-bind:todos="todos"/>
  </div>
</template>

<script>
import Form from './components/Form.vue'
import ImageContainer from './components/ImageContainer.vue'

export default {
  name: 'app',
  components: {
    Form,
    ImageContainer
  }, 
  data() {
    return {
    }
  },
  methods: {
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
  background-color: aliceblue;
  background-repeat: no-repeat;
}
</style>

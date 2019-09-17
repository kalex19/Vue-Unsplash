<template>
  <div class="todo"  >
    <i class="fas fa-star" v-bind:class="{'isStarred':starred}" @click="$emit('star-todo')"></i>
    <input  v-bind:class="{'isCompleted':completed}" :value="text"/>
    <button @click="$emit('line-through')" class="checkBtn">✔️</button>
    <button @click="$emit('del-todo')" class="deleteBtn">X</button>
  </div>
</template>

<script>

export default {
  name: "Todo",
  props: {
    id: Number,
    text: String,
    completed: Boolean,
    starred: Boolean
    }
}

</script>

<style>

.todo {
  display: grid;
  grid-template-columns: 10% 70% 10% 10%;
  justify-content: space-evenly;
  text-align: left;
  width: 35%;
}

input {
  font-size: 2em;
  outline: none;
  background-color: transparent;
  border-color: transparent;
}

.isCompleted {
  text-decoration: line-through;
  text-decoration-color: pink;
}

.fas {
  padding-top: 30%;
  color: white;
}

.isStarred {
 color: rgb(243, 146, 162);
}

.deleteBtn,
.checkBtn {
  border-radius: 50%;
  height: 30px;
  width: 30px;
  font-size: .5em;
  outline: none;
}

</style>

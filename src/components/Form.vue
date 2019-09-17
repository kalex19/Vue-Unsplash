<template>
    <form id="form" @submit="searchIamge">
      <label for="search" class="todoLabel">Search Images</label>
      <input type="text" v-model="text" placeholder="search images here" id="search" class="searchInput">
      <input type="submit" value="Vue Image" class="submitBtn"/>
    </form>
</template>

<script>


export default {
  data() {
    return {
      images: []
    }
  },
  methods: {
    searchImages(e){
      e.preventDefault()
      // const newTodo = {
      //   id: Date.now(),
      //   text: this.text,
      //   completed: false,
      //   starred: false
      // }
      // this.$emit("add-todo", newTodo);
      // this.text = "";
    }
  }
}
</script>

<style>

#form {
  margin: 5%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  width: 50%;
}

.searchLabel {
  font-size: 1.5em;
  font-family: 'Beth Ellen';
}

.searchInput {
  height: 40px;
  width: 300px;
  outline: none;
  font-size: 1.5em;
  background-color: transparent;
  border-color: transparent;
  border-bottom: 2px solid pink;
  font-family: 'Beth Ellen';
  padding-left: 10px;
}

.submitBtn {
  height: 40px;
  width: 100px;
  outline: none;
  font-size: 1.5em;
  background-color: pink;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}

</style>
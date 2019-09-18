<template>
  <main>
    <h1 class="header">Vue Finder</h1>
    <form id="form" @submit="searchIamge">
      <input type="text" v-model="text" placeholder="Search Images Here" id="search" class="searchInput">
      <input type="submit" value="Vue Images" class="submitBtn"/>
    </form>
  </main>
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
           //   fetchImages = (searchTerm) => {
  //     fetch(`https://api.unsplash.com/search/photos/?client_id=${apikey}}?page=1&query=${searchTerm}`)
  //     .then(response => response.json())
  //     .then(images => this.setState({images}))
  //     .catch(error => this.setState({error}))
    }
  }
}
</script>

<style>

#form {
  margin: 2% 15%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  width: 80%;
}

.header {
  margin: 2%;
  font-size: 4em;
  font-family: "Beth Ellen";
  text-decoration: underline pink;
}

.searchInput {
  height: 50px;
  width: 350px;
  outline: none;
  font-size: 1.5em;
  background-color: transparent;
  border-color: transparent;
  border-bottom: 2px solid pink;
  font-family:  Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  padding-left: 10px;
  text-align: center;
}

.submitBtn {
  height: 60px;
  width: 200px;
  outline: none;
  font-size: 1.5em;
  background-color: pink;
  font-family:"Beth Ellen";
}

</style>
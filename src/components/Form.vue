<template>
  <main>
    <h1 class="header">Vue Finder</h1>
    <form id="form" @submit="findImages">
      <input type="text" v-model="searchTerm" placeholder="Search Images Here" id="search" class="searchInput">
      <input type="submit" value="Vue Images" class="submitBtn"/>
    </form>
  </main>
</template>

<script>
export default {
  data() {
    return {
      searchTerm: ""
    }
  },
  methods: {
    findImages: function(e){
      e.preventDefault()
      this.$emit("search-term", this.searchTerm);
       this.searchTerm = "";
    }
  },
}
</script>

<style>
#form {
  margin: 2% 15%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  width: 70%;
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
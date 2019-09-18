<template>
  <div id="app">
    <Form v-on:search-term="findImages"/>
    <ImageContainer :images="images" :error="error"/>
  </div>
</template>

<script>
import Form from "./components/Form.vue";
import ImageContainer from "./components/ImageContainer.vue";
import { apikey } from "./Utils/apikey";
import _ from "lodash";

export default {
  name: "app",
  components: {
    Form,
    ImageContainer
  },
  data() {
    return {
      images: [],
      error: ""
    };
  },
  methods: {
    findImages: _.debounce(async function(searchTerm) {
      try {
        const response = await fetch(
          `https://api.unsplash.com/search/photos/?query=${searchTerm}`,
          {
            headers: { Authorization: `Client-ID ${apikey}` }
          }
        );
        const images = await response.json();
        this.images = images.results;
      } catch (error) {
        this.error = error.message;
      }
    }, 1000)
  }
};
</script>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html,
body {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: aliceblue;
  background-repeat: no-repeat;
}
</style>

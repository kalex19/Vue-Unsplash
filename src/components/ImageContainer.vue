<template>
  <main id="imageContainer">
    <h2 class="error" v-if="error">{error}</h2>
    <section class="images" v-else v-for="image in images" :key="image.id">
      <Unsplash v-bind="image"/>
    </section>
  </main>
</template>

<script>
import Unsplash from "./Unsplash.vue";
export default {
  name: "ImageContainer",
  components: {
    Unsplash
  },
  props:{
    images: Array,
    error: String
  },
}
</script>

<style>
#imageContainer {
  display: grid;
  grid-template-columns: 25% 25% 25% 25%;
  justify-content: space-evenly;
  margin: 5%;
  width: 90%;
}

.error {
  font-size: 1em;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  margin: 5%;
}

.images {
  margin: 2%;
  border: black solid 5px;
  background-color: pink;
  padding: 5%;
  border-radius: 10%;
  /* height: fit-content; */
}
</style>

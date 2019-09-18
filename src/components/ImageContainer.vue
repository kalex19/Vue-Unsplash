<template>
  <main id="imageContainer">
    <h2 v-if="error">{error}</h2>
    <section v-else v-for="image in images" v-bind:key="image.id">
      <Image :url="image.urls.small" :tag="image.alt_description" :user="image.user"/>
    </section>
  </main>
</template>

<script>
import Image from "./Image.vue";
export default {
  name: "ImageContainer",
  components: {
    Image
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
  grid-template-columns: 33% 33% 33%;
  justify-content: space-evenly;
  text-align: left;
  margin: 2%;
  width: 100%;
  transform: rotate(345deg);
}
</style>

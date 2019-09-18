<template>
  <section id="todoContainer">
     <div v-bind:key="image.id">
      <Todo v-bind="image"/>
    </div>
    <div v-bind:key="image.id">
      <Todo v-bind="image"/>
    </div>
  </section>
</template>

<script>
import Image from "./Image.vue";
import apiKey from "../Utils/apikey";
export default {
  name: "ImageContainer",
  components: {
    Image
  },
  props:["images"],
}
</script>

<style>

#imageContainer {
  margin: 15% 30%;
  width: 60%;
  transform: rotate(345deg);
}

</style>

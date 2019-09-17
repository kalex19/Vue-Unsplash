<template>
  <div class="image">
  <image src="" alt="image from unsplash"></image>
  </div>
</template>

<script>
export default {
  name: "Image",
  props: {
    id: Number,
    }
}
</script>

<style>
.image {
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

</style>

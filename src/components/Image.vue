<template>
  <div class="image">
  <image :src=url :alt=tag></image>
  <p>{{user.first_name}} {{user.last_name}}, {{user.instagram_username}}</p>
  <i class="far fa-heart"><p>{{image.likes}}</p></i>
  </div>
</template>

<script>
export default {
  name: "Image",
  props: {
    user: Object,
    url: String,
    tag: String,
    }
}
</script>

<style>
.image {
  background-color: aqua;
}

.fa-heart {
  padding: 2%;
}

p {
  font-size: 1em;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}
</style>

<template>
  <section>
    <img :src="urls.thumb" :alt="alt_description" class="image"/>
    <article class="imageInfo">
      <p>Taken By: {{user.first_name}} {{user.last_name}}</p> 
      <p><i class="far fa-heart"></i> on Instagram @{{user.instagram_username}}</p>
    </article>
  </section>
</template>

<script>
export default {
  name: "Unsplash",
  props: {
    likes: Number,
    user: Object,
    urls: Object,
    alt_description: String,
    }
}
</script>

<style>

.image {
  border-radius: 50%;
}

.imageInfo {
  display: grid;
  grid-template-rows: 50% 50%;
  justify-content: space-evenly;
  margin: 5%;
}

.fa-heart {
  padding: 2%;
}

p {
  font-size: 1em;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  margin: 1%;
}
</style>

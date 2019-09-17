<template>
  <div id="header" >
    <h1>{{title}}</h1>
  </div>
</template>

<script>

export default {
  data() {
    return {
      title: 'Vue Your Todos'
      }
  }
}
</script>

<style>

#header {
  border-bottom: 5px dotted black;
}

h1 {
  color: pink;
  font-size: 4em;
}

</style>

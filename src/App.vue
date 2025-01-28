<template>
  <div v-for="(obj, index) in todos" v-bind:key="obj.id">
    <h1> {{ index }} - {{ obj.name }}</h1>
  </div> 
  <img alt="Vue logo" src="./assets/logo.png">
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      todos: [
          {
            "id": 1,
            "name": "Alice",
            "data": "2025-01-28"
          },
          {
            "id": 2,
            "name": "Bob",
            "data": "2025-01-28"
          },
          {
            "id": 3,
            "name": "Carlos",
            "data": "2025-01-28"
          },
          {
            "id": 4,
            "name": "Diana",
            "data": "2025-01-28"
          },
          {
            "id": 5,
            "name": "Evelyn",
            "data": "2025-01-28"
          }
      ]
  }
}
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

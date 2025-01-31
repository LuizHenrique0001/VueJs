<template>
  fullName: {{ fullName }}
  <nav>
    
    <div >
      <h3>Usuarios Ativos</h3>
      <p v-for=" obj in unStatusTrue" :key="obj.id" >
        {{ obj.name }} - {{ obj.age }} - {{ obj.id }}
      </p>
    </div>
    
    
    <div >
      <h3>Usuarios Desativados</h3>
      <p v-for=" obj in unStatusFalse" :key="obj.id" >
        {{ obj.name }} - {{ obj.age }} - {{ obj.id }}
      </p>
    </div>
    
    
    <div >
      <h3>obj Usuarios</h3>
      <p v-for=" obj in findAll" :key="obj.id" >
        <input type="checkbox" v-model="obj.status" />
        {{ obj.name }} - {{ obj.age }} - {{ obj.id }}
      </p>
    </div>
    
  </nav>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      user: {
        name: 'John Doe',
        age: 30
      },
      todos: 
      [
        {
          "id": 1,
          "name": "Ana",
          "age": 25,
          "status": true
        },
        {
          "id": 2,
          "name": "Bruno",
          "age": 30,
          "status": false
        },
        {
          "id": 3,
          "name": "Clara",
          "age": 22,
          "status": true
        },
        {
          "id": 4,
          "name": "Diego",
          "age": 28,
          "status": false
        },
        {
          "id": 5,
          "name": "Eva",
          "age": 27,
          "status": true
        },
        {
          "id": 6,
          "name": "Fábio",
          "age": 26,
          "status": false
        },
        {
          "id": 7,
          "name": "Gisele",
          "age": 24,
          "status": true
        },
        {
          "id": 8,
          "name": "Hugo",
          "age": 29,
          "status": false
        },
        {
          "id": 9,
          "name": "Isabela",
          "age": 23,
          "status": true
        },
        {
          "id": 10,
          "name": "João",
          "age": 31,
          "status": false
        }
      ],
    }
  },
  computed: {
    // Add your computed properties here
    fullName(){
      return `${this.user.name} ${this.user.age}`
    },
    unStatusTrue(){
      return this.todos.filter(todo => todo.status === true)
    },
    unStatusFalse(){
      return this.todos.filter(todo => todo.status === false)
    },
    findAll(){
      return this.todos
    }
  },
  methods: {
    // Add your methods here
  }
}

</script>
<style>
.text {
  color: blue;
  font-size: 30px;
  font-family: Arial, sans-serif;
}
.title {
  color: red;
  font-size: 60px;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
div{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  border: 1px solid black;
  width: 50%;
  flex-direction: column;
}
nav{
  display: flex;
  
}
</style>

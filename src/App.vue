<template>
  <div>
     <button @click.once="onclick">Enviar</button>
     <h2></h2>
  </div> 
  <br><br>
  <div>
    <button @mousemove="mover">opa</button>
  </div>
  <br><br>
  <form action="https://google.com" @submit.prevent="onSubmit">
    <input type="text"  @keyup="onKeyup" id="">
    <button type="submit">
      Enviar
    </button>
  </form>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
     
    }
  },
  methods: {
    onclick($evt){
      console.log('clicou', $evt)
    },
    mover($evt){
      console.log('Estas moviendo el mouse', $evt)
    },
    onSubmit(){
      console.log('Formulario enviado')
    },
    onKeyup($evt){
      console.log('Estas escribiendo', $evt)
    }
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
</style>

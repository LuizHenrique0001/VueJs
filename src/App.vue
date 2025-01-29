<template>
  <div>
    <div>
      one way binding<br>
      Two way binding<br>
      v-model formularios
    </div>
    <br>
    <br>
    <div>
      <label for="">Nome</label><br>
      <input type="text" v-model="name">
      <br>
      {{ name }}
    </div>
    <br><br>
    <div>
      <label for="">Carro</label><br>
      <select v-model="carr">
        <option value="">Escolha</option>
        <option value="volvo">Volvo</option>
        <option value="saab">Saab</option>
        <option value="mercedes">Mercedes</option>
        <option value="audi">Audi</option>
      </select>
      <br>
      {{ carr }}
    </div>
    <br><br>
    <div>
      <label for="">Noticia</label>
      <input type="radio" value="sim" v-model="noticia">Sim
      <input type="radio" value="nao" v-model="noticia">Nao
      <br><br>
      {{ noticia }}
    </div>
    <div>
      <label for="">Contrato</label><br>
      <input type="checkbox" value="sim" v-model="contrato">Aceita Nosso...
      <br><br>
      {{ contrato }}
    </div>
    <br><br>
    <div>
      <label for="">Cores</label><br>
      <input type="checkbox" value="Amarelo" v-model="cores">Amarelo
      <input type="checkbox" value="Vermelho" v-model="cores">Vermelho
      <input type="checkbox" value="Azul" v-model="cores">Azul
      <br><br>
      {{ cores }}
    </div>
  </div> 
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      name: 'Luiz Henrique',
      carr: '',
      noticia: '',
      contrato: false,
      cores: []
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

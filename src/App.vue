<template>
  <div>
    <div>
      One-way data binding <br>
      Two-way data binding <br>
      v-model -> formulários
    </div>

    <br><br>

    <div>
      <label>Nome</label> <br>
      <input 
        type="text"
        v-model="name"
      > <br>
      {{ name }}
    </div>

    <br><br>

    <div>
      <label>Esportes</label> <br>
      <select v-model="esportes">
        <option value="">Escolha</option>
        <option value="futebol">Futebol</option>
        <option value="volei">Volei</option>
        <option value="basquete">Basquete</option>
      </select> <br>
      {{ esportes }}
    </div>

    <br><br>

    <div>
      <label>Newsletter</label> <br>
      <input 
      v-model="newsletter"
        type="radio"
        value="Sim"
      > Sim
      
      <input 
        v-model="newsletter"
        type="radio" 
        value="Não"
      > Não <br>
      {{ newsletter }}
    </div>

    <br><br>
    
    <div>
      <label>Contrato</label> <br>
      <input 
      v-model="contract"
        type="checkbox"
      > Aceito os termos de uso <br>
      
      {{ contract }}
    </div>

    <br><br>

    <div>
      <label>Cores que você mais gosta</label> <br>
      <input 
      v-model="colors"
        type="checkbox"
        value="Preto"
      > Preto
      <input 
      v-model="colors"
        type="checkbox"
        value="Azul"
      > Azul
      <input 
      v-model="colors"
        type="checkbox"
        value="Vermelho"
      > Vermelho <br>
      
      {{ colors }}
    </div>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheHeader from './components/TheHeader.vue'

export default {
  name: 'App',
  data() {
    return {
      name: 'Digite aqui',
      esportes: '',
      newsletter: '',
      contract: false,
      colors: [],
    }
  }
}
</script>

<style>
label {
  font-weight: bold;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin: 60px;
}
</style>

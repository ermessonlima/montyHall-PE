<template>
  <div id="app">
    <h1>Problema de Monty Hall
      <p>2º P. Estatística e Prob.</p>
    </h1>
       <h1>Encontre a porta com a nota 10 em Estatística e Probabilidade
    </h1>
    <div class="form">
      <div v-if="!started">
        <label for="portsAmount"> Quantas portas? </label>
        <input
          type="text"
          id="portsAmount"
          size="3"
          v-model.number="portsAmount"
        />
      </div>
      <div v-if="!started">
        <label for="selectedPort"> Qual das porta é a premiada? </label>
        <input
          type="text"
          id="selectedPort"
          size="3"
          v-model.number="selectedPort"
        />
      </div>
 
      <button v-if="!started" @click="started = true">Iniciar</button>
      <button v-if="started" @click="started = false">Reiniciar</button>
    </div>

    <div class="doors" v-if="started">
      <div v-for="i in portsAmount" :key="i">
        <Door :hasGift="i === selectedPort" :number="i" />
      </div>
    </div>
   <p>Aluno: Ermesson Lima dos Santos
    </p>
  </div>
  
</template>

<script>
import Door from './components/Door'
export default {
  name: "App",
  components: {
    Door
  },
  data: function () {
    return {
      started: false,
      portsAmount: 3,
      selectedPort: null,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
#app h1 {

  padding: 20px;
  margin-bottom: 60px;
}
body {
  background: linear-gradient(to right, #a8ff78, #78ffd6);
}

.form {
  display:flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 40px;
}

.form, .form input, .form button {
  margin-bottom: 10px;
  font-size: 2rem;
}

.doors {
  align-self: stretch;
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}
</style>

<template>
  <div id="app">
    <h1>Monty Hall Problem</h1>
    <div class="form">
      <div v-if="!started">
        <label for="portsAmount">How many doors?</label>
        <input type="text" id="portsAmount" size="3" v-model.number="portsAmount">
      </div>
      <div v-if="!started">
        <label for="selectedPort">Which door is awarded?</label>
        <input type="text" id="selectedPort" size="3" v-model.number="selectedPort">
      </div>
      <button v-if="!started" @click="started = true">Start</button>
      <button v-if="started" @click="started = false">Restart</button>
    </div>

    <div class="doors" v-if="started">
      <div v-for="i in portsAmount" :key="i">
        <Door :hasGift="i == selectedPort" :number="i" />
      </div>
    </div>

    <Footer />
  </div>
</template>

<script>
import Door from './components/Door.vue'
import Footer from './components/Footer.vue'

  export default {
    name: "App",
    components: {Door, Footer},
    data(){
      return{
        started: false,
        portsAmount: 3,
        selectedPort: null
      }
    }
  };
</script>

<style>
  * {
    font-family: "Montserrat", sans-serif;
    box-sizing: border-box;
  }

  body {
    color: #fff;
    background: linear-gradient(90deg, #222424 10%, #b8b5ae 90%);
  }

  #app {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  #app h1 {
    border: 1px solid #000;
    background-color: #0004;
    padding: 20px;
    margin-bottom: 60px;
  }

  .form{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 40px;
  }

  .form, .form input, .form button{
    margin-bottom: 10px;
    font-size: 1.8rem;
  }

  .doors{
    align-self: stretch;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    max-width: 100%;
  }
</style>

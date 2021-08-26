<template>
  <div id="app">
    <h1>Monty Hall Problem</h1>
    <Door number='1' :hasGift="false" />
  </div>
</template>

<script>
import Door from './components/Door.vue'

  export default {
    name: "App",
    components: {Door},
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
</style>

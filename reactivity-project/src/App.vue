<template>
  <div id="app">
    <img class="main-img" alt="Vue logo" src="./assets/main.jpg">
    <HelloWorld msg="Build your outfit"/>
    <div id="column column 1">Tops</div>
    <div id="column column 2"></div>
    <div id="column column 3"></div>    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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

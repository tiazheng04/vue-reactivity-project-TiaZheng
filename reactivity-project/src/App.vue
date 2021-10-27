<template>
  <div id="app">
    <HelloWorld msg="Build your outfit"/>
    <img class="main-img" alt="Vue logo" src="./assets/main.jpg">
    <div class= "column-container">
      <div class="column column 1">Tops</div>
      <div class="column column 2">xxx</div>
      <div class="column column 3">Footwear</div>  
    </div>
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
  font-size: 62.5%;
  background-color: ;
}
.main-img{
  width: 80vw;
  margin: 2rem 0rem 4rem
}
.column-container{
  display:flex;
  flex-direction: row;
  width:100vw;
  justify-content: space-around;
}
.column{
  width: 17rem
}
</style>

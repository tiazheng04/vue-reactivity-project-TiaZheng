<template>
  <div id="app">
    <HelloWorld msg="Build your outfit"/>
    <img class="main-img" alt="Vue logo" src="./assets/main.jpg">
    <div class= "column-container">
      <div class="column column 1">
        <h2 class="section-name">Tops</h2>
        <h3 class="lists">lists</h3>
      </div>
      <div class="column column 1">
        <h2 class="section-name">xxx</h2>
        <h3 class="lists">lists</h3>
      </div>
      <div class="column column 1">
        <h2 class="section-name">Footwear</h2>
        <h3 class="lists">lists</h3>
      </div>
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
  display: flex;
  flex-direction: column;
  align-items: center;

  font-size: 62.5%;
  background-color: rgb(160, 193, 236);
  height: 100vh;
}
.main-img{
  width: 50vw;
  margin: 2rem 0rem 4rem;
  border-radius: 1rem;
}
.column-container{
  display:flex;
  flex-direction: row;
  width:90vw;
  justify-content: space-around;
  background-color: white;
  height: 40vh;
}
.section-name{
  border: solid;
  border-width: .1rem;
}

.column{
  width: 15rem;
  height: 35vh;
  
}

.lists{
  border-left: dashed;
  border-width: .1rem;
  background-color: blue;
  height: 20rem;
  width: 14rem;
}

</style>

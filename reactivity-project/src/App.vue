<template>
  <div id="app">
    <HelloWorld msg="Build your outfit"/>
    <img class="main-img" alt="Vue logo" src="./assets/main.jpg">
    <section class="box">
      <section class= "column-container">
        <div class="column column1">
          <h2 class="section-name">Tops</h2>
          <h3 class="lists">lists</h3>
        </div>
        <div class="column column2">
          <h2 class="section-name">xxx</h2>
          <h3 class="lists">lists</h3>
        </div>
        <div class="column column3">
          <h2 class="section-name">Footwear</h2>
          <h3 class="lists">lists</h3>
        </div>
        <button>Next</button>
      </section>
      <section class="img-preview">box</section>
      <section class="cart">another box</section>
    </section>

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
  padding: 2rem;
  font-size: 62.5%;
  background-color: rgb(160, 193, 236);
  height: auto;
}
.main-img{
  width: 30vw;
  margin: 2rem 0rem 4rem;
  border-radius: 1rem;
}
.column-container{
  display:flex;
  flex-direction: column;
  width:30vw;
  justify-content: space-around;
  background-color: white;
  height: 30rem;
  align-items: center;
  border-radius: 2rem;
  padding: 3rem 0rem;
  
}
.section-name{
  border: solid;
  border-width: .1rem;
  padding: 0.5rem 3rem;
}

.column{
  width: 20rem;
  height: 25rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  /* background-color: yellow; */
  padding-bottom: 2rem;

}

.lists{
  border-left: dashed;
  border-width: .1rem;
  background-color: blue;
  height: 20rem;
  width: 18rem;
  border-radius: 0.4rem;
}

.box{
  display: flex;
  flex-direction: row;
  width: 100vw;
  justify-content: space-around;
}

.img-preview{
  background-color: orange;
}

.cart{
  background-color: green;
}
.column2{
  display: none;
}

.column3{
  display: none;
}

</style>

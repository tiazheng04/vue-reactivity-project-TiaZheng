<template>
  <div id="app">
    <HelloWorld msg="Shop"/>
    <img :src="image" class="main-img" alt="Vue logo">
    <section class="box">
      <section class= "column-container">
        <h2 class="section-name">Selections</h2>
        <div class="column">
          <div v-for="product in types" :key="product" class="lists">
            <div>{{product.item}}</div>
            <img class="img" :src="product.variantImage">
          </div>
        </div>
      </section>
      <section class="cart">
        <button @click ="cart()">Cart</button>
      </section>
    </section>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return{

      cart: 0,
      product: "Tops",
      brand: "Vue Sadness",
      image: require('./assets/main.jpg'),
      types: [
        {
        item: "Black Shirt",
        variantImage: require('./assets/blackShirt.jpg'),
        cost: "$10"
        },
                {
        item: "Blue Button Down",
        variantImage: require('./assets/blueButton.jpg'),
        cost: "$10"
        },
                {
        item: "Blue Hoodie",
        variantImage: require('./assets/blueHoodie.jpg'),
        cost: "$10"
        },
                {
        item: "White Shirt",
        variantImage: require('./assets/whiteShirt.jpg'),
        cost: "$10"
        },
                {
        item: "Black Zip Hoodie",
        variantImage: require('./assets/zip.jpg'),
        cost: "$10"
        },

      ],


      methods: {
        cart(){
          this.cart +=1
        },
        total(){
          this.total +=10
        }
      }

    }

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
  width:60vw;
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
  /* display: flex;
  flex-direction: row; */
  align-items: center;
  background-color: yellow;
  padding-bottom: 2rem;

}

.lists{
  /* border-left: dashed; */
  border-width: .1rem;
  /* background-color: blue; */
  height: 20rem;
  /* width: 18rem; */
  border-radius: 0.4rem;
  font-size: 1rem;
 /*  display: flex;
  flex-direction: row; */
}

.box{
  display: flex;
  flex-direction: row;
  width: 100vw;
  justify-content: space-around;
}



.cart{
  background-color: green;
  width: 20vw;
}


.img{
  width: 20rem;
  height: 20rem;
  border-style: solid;
  display: flex;
  flex-direction: row;
  
}

</style>

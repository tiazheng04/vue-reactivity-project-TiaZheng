<template>
  <div id="app">
    <HelloWorld msg="Shop"/>
    <img :src="mainImage" class="main-img" alt="Vue logo">
    <section class="box">
      <section class= "column-container">
        <h2 class="section-name">Selections</h2>
        <div class="column">
          <div v-for="type in types" :key="type.id" class="lists" id="lists">
            <div @click="displayImg(type.variantImage)" class="types">
              <div class="itemName">{{type.item}}</div>
              <button v-on:click="displayCart(types)">Add to Cart</button>
            </div>
          </div>  

          <!-- <div v-for="item in types" :key="item" class="lists" id="lists">
            <div @click="() => displayCart(item)" class="types">
              {{item.text}}
            </div>
          </div>  -->
        </div>
      </section>
      <section class="img-box">
        <img :src="image" alt="nothing" class="img">
      </section>
      <section class="details">

      </section>
      <section class="cart">
        <p>Cart({{cartValue}})</p>
        <p  class="cart-list">{{cartList}}</p>
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

      cartValue: 0,
      cartList:[],
      detail: [],
      product: "Tops",
      brand: "Vue Sadness",
      image: require('./assets/placeholder.jpg'),
      mainImage: require('./assets/main.jpg'),
      types: [
        {
        item: "Black Shirt",
        variantImage: require('./assets/blackShirt.jpg'),
        variantDetails:["100% cotton", "abcdef", "dark wear"],
        id:1
        },
                {
        item: "Blue Button Down",
        variantImage: require('./assets/blueButton.jpg'),
        variantDetails:["90% cotton", "ghijk", "casual wear"],
        id:2
        },
                {
        item: "Blue Hoodie",
        variantImage: require('./assets/blueHoodie.jpg'),
        variantDetails:["80% cotton", "lmnop", "comfort wear"],
        id:3
        },
                {
        item: "White Shirt",
        variantImage: require('./assets/whiteShirt.jpg'),
        variantDetails:["70% cotton", "qrstu", "light wear"],
        id:4
        },
                {
        item: "Black Zip Hoodie",
        variantImage: require('./assets/zip.jpg'),
        variantDetails:["60% cotton", "vwxyz", "winter wear"],
        id:5
        },

      ], 
      


    








    }

  },

        methods: {
        addToCart() {
          this.cartValue += 1;
        },



        // Information(details) {
        //   this.detail.push(details)
        // },

        displayImg(variantImage) {
          this.image = variantImage
        },

        displayCart(types) {
          this.cartValue += 1;
          this.cartList.push(types)
          console.log(this.cartList)

        },
      },
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
  width: 30rem;
  height: 15rem;
  margin: 2rem 0rem 4rem;
  border-radius: .5rem;
}
.column-container{
  display:flex;
  flex-direction: column;
  width:35vw;
  justify-content: space-around;
  background-color: white;
  height: 20rem;
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
  height: 20rem;
  /* display: flex;
  flex-direction: row; */
  align-items: center;
  background-color: rgb(166, 160, 172);
  padding-bottom: 1rem;

}

.lists{
  border-width: .1rem;
  height: 4rem;
  border-radius: 0.4rem;
  font-size: 1rem;
  display: flex;
  flex-direction: column; 
  align-items: center;
}

.box{
  display: flex;
  flex-direction: row;
  width: 100vw;
  justify-content: space-evenly;
}



.cart{
  background-color: rgb(37, 64, 73);
  width: 20vw;
  height: 50vh;
  color: white;
}


.img-box{
  width: 20rem;
  height: 20rem;
  border-style: solid;
  
}

.img{
  height: 20rem;
  width: 20rem;
}

.types{
  border-style: solid;
  width: 10rem;
  padding: .3rem;
}

.itemName{
  margin-bottom: 0.5rem;
  font-size: .8rem;
}


</style>

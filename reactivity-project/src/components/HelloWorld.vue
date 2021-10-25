<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

  </div>

  var app = new({
    el: '#app',
    data: {
      product: 'Socks',
      image: ./src/assets/blackShirt.jpg
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>


<style scoped>

</style>

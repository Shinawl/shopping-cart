<template>
  <h1>Produits dans mon panier</h1>
 <ul>
 <li v-for="item in cart" v-bind:key={item}>{{item}}</li>
 </ul>
 
 <button v-on:click="$emit('enlarge-text')">Agrandir texte</button>
 
 <button v-on:click="$emit('update-cart', cart)">Passer ma commande</button>
 
</template>

<script>
export default {
 name: 'HelloWorld',
 data(){
 return {
 cart: ['pain', 'fromage', 'fleurs', 'vin']
 }
 },
 props: {
 msg: String
 }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

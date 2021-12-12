<template>
  <img alt="Vue logo" src="./assets/logo.png">
 <h1 :style="{ fontSize: postFontSize + 'em' }">Le titre de mon site</h1>
 <HelloWorld 
 v-on:enlarge-text="postFontSize += 0.1" 
 @update-cart="updateCart"
 msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
 
export default {
 name: 'App',
 components: {
 HelloWorld
 },
 data(){
 return {
 postFontSize: 1
 }
 },
 methods: {
 updateCart(toto) {
 console.log("mettre à jour panier");
 console.log(toto)
 //this.cart.push(e);
 //this.total = this.shoppingCartTotal;
 },
 emptyCart() {
 console.log('vider mon panier')
 }
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
  margin-top: 60px;
}
</style>

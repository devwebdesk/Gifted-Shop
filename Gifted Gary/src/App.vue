<template>
  <div id="app">
   
    <HelloWorld/>
    <!-- <REmail /> -->
    <!-- <CheckoutEmail btntext="xyz" /> -->
    <!-- <ConfirmEmail/> --> 

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import ConfirmEmail from './components/ConfirmEmail.vue'
// import CheckoutEmail from './components/CheckoutEmail.vue'
// import REmail from './components/REmail.vue'

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

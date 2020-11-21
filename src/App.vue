<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Supermarket list :D"/> -->
    <Count/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Count from './components/SupermarketList.vue'

export default {
  name: 'App',
  components: {
    Count
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

ol li{
  text-align: left !important;
}
</style>

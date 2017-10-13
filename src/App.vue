<template>
  <div id="app">
    <tr-header></tr-header>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import TrHeader from './components/GvHeader'

export default {
  name: 'app',
  components: {
    TrHeader,
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
}
body, html {
  margin: 0;
  background-color: #000;
  height: 100%;
}
</style>

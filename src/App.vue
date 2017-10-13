<template>
  <div id="app">
    <tr-header></tr-header>
    <gv-main class="main"></gv-main>
    <gv-ticker></gv-ticker>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import TrHeader from './components/GvHeader'
import GvTicker from './components/GvTicker'
import GvMain from './components/GvMain.vue'

export default {
  name: 'app',
  components: {
    TrHeader,
    GvMain,
    HelloWorld,
    GvTicker
  }
}
</script>

<style>
  body, html {
    margin: 0;
    background-color: #000;
    height: 100%;
    color: #fff;
  }
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  display: flex;
  flex-direction:column;
}
  .main{
    flex: 1;
  }
</style>

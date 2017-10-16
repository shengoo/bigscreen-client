<template>
  <div id="app">
    <tr-header></tr-header>
    <div class="main">
      <gv-main class="main-content"></gv-main>
      <gv-side class="side"></gv-side>
    </div>
    <gv-ticker></gv-ticker>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import TrHeader from './components/GvHeader'
import GvTicker from './components/GvTicker'
import GvMain from './components/GvMain.vue'
import GvSide from './components/GvSide.vue'
import GvVideo from './components/GvVideo.vue'

export default {
  name: 'app',
  components: {
    GvSide,
    TrHeader,
    GvMain,
    HelloWorld,
    GvTicker,
    GvVideo
  }
}
</script>

<style>
  * {
    font-family: KnowledgeMedium, sans-serif;
  }
  body, html {
    margin: 0;
    background-color: #000;
    height: 100%;
    color: #fff;
  }
  #app {
    /*font-family: 'Avenir', Helvetica, Arial, sans-serif;*/
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    height: 100%;
    display: flex;
    flex-direction:column;
  }
  .main{
    flex: 1;
    display: flex;
    align-items:stretch;
  }
  .main-content{
    flex:1;
  }
  .side{
    width: 286px;
  }
</style>

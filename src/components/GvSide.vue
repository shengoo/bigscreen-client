<template>
  <div class="container">
    <gv-video></gv-video>
  </div>
</template>

<script>
  import GvVideo from './GvVideo.vue'
  export default {
    name: 'GvSide',
    components: {GvVideo},
    data () {
      return {
      }
    },
    created: function () {
      // `this` 指向 vm 实例
    },
    destroyed: function () {
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  * {
    font-family: KnowledgeMedium, sans-serif;
  }

  .container {
    background-color: #333;
    display: flex;
    flex-direction:column;
    align-items: center;
  }

</style>

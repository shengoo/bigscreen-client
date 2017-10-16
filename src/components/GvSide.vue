<template>
  <div class="container">
    <gv-video></gv-video>
    <gv-code></gv-code>
  </div>
</template>

<script>
  import GvVideo from './GvVideo.vue'
  import GvCode from './GvCode.vue'
  export default {
    name: 'GvSide',
    components: {
      GvVideo,
      GvCode
    },
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
    justify-content: space-between;
  }

</style>

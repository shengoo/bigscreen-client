<template>
  <div class="container">
    <video
      src="../assets/sample.mov"
      autoplay loop autobuffer></video>
  </div>
</template>

<script>
  export default {
    name: 'GvVideo',
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

  .container {
    background-color: #444;
    width: 286px;
    display: flex;
    align-items: center;
  }

  video{
    width:100%;
  }

</style>

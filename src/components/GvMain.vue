<template>
  <div class="container">
    Main
  </div>
</template>

<script>
  export default {
    name: 'GvMain',
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
    /*height:33px;*/
    display: flex;
    align-items: center;
    background-image: url("../assets/background_image (1).jpg");
    background-size: 100% 100%;
  }

</style>

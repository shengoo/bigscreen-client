<template>
  <div class="container">
    <span>
      Join US on Wechat Scan QR Code Follow TR_Community
    </span>
    <img src="../assets/TR_Community.png" width="90">
  </div>
</template>

<script>
  export default {
    name: 'GvCode'
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container{
  display: flex;
  flex-direction: row;
}
  span{
    flex: 5;
    text-align: left;
    padding-left: 10px;
    font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
    font-size: 14px;
    font-weight: bold;
    vertical-align: middle;
    display: inline-block;
    line-height: 1.5;
  }
  img{
    flex: 3;
    padding:5px;
  }
</style>

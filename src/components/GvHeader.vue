<template>
  <div class="container">
    <div class="gv_logo">
      <img src="../assets/logo.png"/>
    </div>
    <div class="gv_time_style">
    <span id="gv_date" class="gv_date">
      {{date.toLocaleDateString()}}
    </span><br>
      <span id="gv_time" class="gv_time">
      {{date.toLocaleTimeString('en-us', options)}}
    </span>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'TrHeader',
    data () {
      const options = {
        hour: '2-digit', minute: '2-digit'//, second: '2-digit'
      }
      return {
        options: options,
        date: new Date()
      }
    },
    created: function () {
      // `this` 指向 vm 实例
      this.interval = setInterval(() => {
        this.date = new Date()
      }, 1000)
    },
    destroyed: function () {
      clearInterval(this.interval)
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  * {
    font-family: 'KnowledgeMedium';
  }

  .container {
    background-color: rgb(37, 37, 41);
    color: #fff;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .gv_date {
    font-weight: bold;
    font-size: 30px;
  }

  .gv_time {
    font-weight: bold;
    font-size: 25px;
  }
</style>

<template>
  <div class="container">
    数据来源：Thomson Reuters
    <transition name="fade">
      <div v-show="showing === 'Currencies'" key="Currencies">Currencies： GBP/CNY 8.74 1.09% USD/CNY 6.59 0.00% EUR/CNY 7.79 -0.03% USD/JPY 112.11 -0.14%</div>
    </transition>
    <transition name="fade">
      <div v-show="showing === 'Equities'" key="Equities">Equities： TRI 46.43 0.24% CITI 72.37 -3.43% IBM 147.03 -0.40% LeTV 30.68 0.00%</div>
    </transition>
    <transition name="fade">
      <div v-show="showing === 'Commodities'" key="Commodities">Commodities： LCOc1 57.19 1.07 CLc1 51.35 0.83 Gold 1293.75 0.35 Silver 17.23 0.06</div>
    </transition>
  </div>
</template>

<script>
//  const defalut = {
//    fx:
//  }
  const types = ['Currencies', 'Equities', 'Commodities']
  export default {
    name: 'GvTicker',
    data () {
      return {
        showing: 'Currencies'
      }
    },
    created: function () {
      // `this` 指向 vm 实例
      this.count = 0
      this.interval = setInterval(() => {
        this.showing = types[++this.count % 3]
      }, 3000)
    },
    destroyed: function () {
      clearInterval(this.interval)
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  * {
    font-family: KnowledgeBold,SimHei;
  }

  .container {
    background-color: #222;
    height:33px;
    display: flex;
    align-items: center;
  }

</style>

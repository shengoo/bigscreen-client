<template>
  <div class="container">
    <div>Source：Thomson Reuters</div>
    <div class="content">
      <transition name="cube-top">
        <div class="row" v-if="showing === 'Currencies'" key="Currencies">
          <div class="label">Currencies：</div>
          <div class="item">
            <div>GBP/CNY</div>
            <div>8.74</div>
            <div>1.09%</div>
          </div>
          <div class="item">
            <div>GBP/CNY</div>
            <div>8.74</div>
            <div>1.09%</div>
          </div>
        </div>
        <!--</transition>-->
        <!--<transition :duration="2000" name="fade">-->
        <div class="row" v-if="showing === 'Equities'" key="Equities">
          <div class="label">Equities：</div>
          <div class="item">
            <div>GBP/CNY</div>
            <div>8.74</div>
            <div>1.09%</div>
          </div>
          <div class="item">
            <div>GBP/CNY</div>
            <div>8.74</div>
            <div>1.09%</div>
          </div>
        </div>
        <!--</transition>-->
        <!--<transition :duration="2000" name="fade">-->
        <div class="row" v-if="showing === 'Commodities'" key="Commodities">
          <div class="label">Commodities：</div>
          <div class="item">
            <div>LCOc1</div>
            <div>57.19</div>
            <div>1.07</div>
          </div>
          <div class="item">
            <div>GBP/CNY</div>
            <div>8.74</div>
            <div>1.09%</div>
          </div>
        </div>
      </transition>
    </div>
  </div>
</template>

<script>
//  const defaultExchangeRics = 'GBPCNY=CNY=EURCNY=JPY='
//  const defaultEquityRics = 'TRI.N,C.N,IBM.N,300104.SZ'
//  const defaultCommodityRics = 'LCOc1,CLc1,XAU=X,XAG=X'
//  const defaultFields = 'BID,NETCHNG_1,PCTCHNG,BID_TICK_1,TRDPRC_1,HST_CLOSE,PRCTCK_1,ASK,CF_LAST,DSPLY_NAME,CF_NETCHNG,CF_TICK,CF_CLOSE'
  const types = ['Currencies', 'Equities', 'Commodities']
  export default {
    name: 'GvTicker',
    data () {
      return {
        showing: types[0]
      }
    },
    created: function () {
      // `this` 指向 vm 实例
      this.count = 0
      this.interval = setInterval(() => {
        this.showing = types[++this.count % 3]
      }, 3000)
      fetch('http://localhost:49957/api/quotes/quoteswihoutcache?symbols=TRI.N,C.N,IBM.N,300104.SZ&fields=BID,NETCHNG_1,PCTCHNG,BID_TICK_1,TRDPRC_1,HST_CLOSE,PRCTCK_1,ASK,CF_LAST,DSPLY_NAME,CF_NETCHNG,CF_TICK,CF_CLOSE')
    },
    destroyed: function () {
      clearInterval(this.interval)
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  * {
    font-family: KnowledgeBold, SimHei;
  }

  .container {
    background-color: #222;
    height: 33px;
    display: flex;
    align-items: center;
    padding: 0 10px;
  }

  .content {
    flex: 1;
    display: flex;
    align-items: center;
    padding-left: 20px;
  }

  .row {
    position: absolute;
    flex: 1;
    display: flex;
    flex-direction: row;
  }

  .row .label {
    /*position: fixed;*/
  }

  .item {
    display: flex;
    flex-direction: row;
    padding: 0 10px;
  }

  .item > div {
    padding: 0 5px;
  }

  .cube-top-enter-active {
    animation: cube-top-in .5s;
  }

  .cube-top-leave-active {
    animation: cube-top-out .5s;
  }

  @keyframes cube-top-in {
    from {
      transform: translateY(100%) rotateX(90deg);
      transform-origin: top;
    }
    to {
      transform: rotateX(0)
    }
  }

  @keyframes cube-top-out {
    to {
      transform: translateY(-100%) rotateX(-90deg);
      transform-origin: bottom;
    }
  }

</style>

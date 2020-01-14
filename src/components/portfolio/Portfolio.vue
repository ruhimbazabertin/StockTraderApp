<template>
  <div>
      <trader-stock v-for="stock in stocks" :stock="stock"></trader-stock>
  </div>
</template>

<script>
import {mapGetters} from 'vuex'
import Stock from './Stock'
export default {
       computed: {
          ...mapGetters({
                stocks: 'stockPortfolio'
          })
       },
      components: {
          'trader-stock': Stock,
      }
}
</script>

<style>

</style>
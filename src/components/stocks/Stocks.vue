<template>
   <div>
       <trader-stock v-for="stock in stocks" :key="stock.index" :stock="stock"></trader-stock>
   </div>
</template>

<script>
import Stock from '../stocks/Stock'
export default {
      components: {
          'trader-stock': Stock,
      },
      computed: {
        stocks() {
            return this.$store.getters.stocks;
        }
      }
}
</script>

<style>

</style>
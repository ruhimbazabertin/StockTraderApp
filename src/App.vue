<template>
  <div class="container">
    <trader-header> </trader-header>
    <div class="row">
      <div class="col-xs-12">
            <router-view></router-view>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/Header'
export default {
      components: {
        'trader-header': Header,
      },
      created(){
        this.$store.dispatch('initStocks');
      }
}
</script>

<style>
body{
  padding: 30px;
}
</style>
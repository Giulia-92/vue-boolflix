<template>
  <div id="app">
    <HeaderContent/>
    <CardContent/>
  </div>
</template>

<script>
import HeaderContent from './components/HeaderContent.vue'
import CardContent from './components/CardContent.vue'
export default {
  name: 'App',
  components: {
   HeaderContent,
   CardContent
  }
  
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

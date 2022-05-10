<template>
  <div id="app">
    <HeaderContent/>
  </div>
</template>

<script>
import HeaderContent from './components/HeaderContent.vue'

export default {
  name: 'App',
  components: {
   HeaderContent
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

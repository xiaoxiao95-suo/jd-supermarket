<template>
  <div id="app">
    <nav-menu></nav-menu>
    <header-search></header-search>
    
  </div>
</template>

<script>

import HeaderSearch from './components/HearSearch/index'
import NavMenu from './components/navMenu/index'
export default {
  name: 'App',
  components: {
    HeaderSearch,
    NavMenu
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>

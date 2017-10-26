<template>
  <div id="app">
    <menu-header></menu-header>
    <router-view/>
  </div>
</template>

<script>
import MenuHeader from '@/components/MenuHeader'

export default {
  name: 'app',

  components: {
    MenuHeader
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
body {
  margin: 0px
}
</style>

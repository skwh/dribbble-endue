<template>
<div id="app">
  <endue-header></endue-header>
  <endue-main></endue-main>
  <div id="articles">

  </div>
</div>
</template>

<script>
import EndueHeader from './components/Header'
import EndueMain from './components/Main'

export default {
  name: 'app',
  components: { EndueHeader, EndueMain }
}
</script>

<style lang="scss">
$main-black: #0B1227;
$main-red: #FD455f;

*, *::before, *::after {
  box-sizing: border-box;
}

html, body {
  padding: 0;
  margin: 0;
  background-color: black;
}

#app {
  font-family: 'Raleway', sans-serif;
  font-weight: bold;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
}
</style>

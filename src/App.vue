<template>
<div id="app">
  <endue-header></endue-header>
  <main>
    <endue-main></endue-main>
    <endue-articles></endue-articles>
  </main>
</div>
</template>

<script>
import EndueHeader from './components/Header'
import EndueMain from './components/Main'
import EndueArticles from './components/Articles'

export default {
  name: 'app',
  components: { EndueHeader, EndueMain, EndueArticles }
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
  background-image: url('https://j.gifs.com/9QkyKB.gif');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

#app {
  font-family: 'Raleway', sans-serif;
  font-weight: bold;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
}

main {
  margin-left: 280px;
  margin-right: 280px;
}
</style>

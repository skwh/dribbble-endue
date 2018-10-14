<template>
  <header>
    <div id="logo">
      <logo-icon :topColor="this.main_black"
                 :bottomColor="this.main_red"></logo-icon>
      <span>endue<sup>&reg;</sup></span>
      <span class="bar"></span>
    </div>
    <nav>
      <a v-for="(pageName, index) in pages"
           :key="`link-${index}`"
           class="navigation-item"
           href="#">
        <material-icon v-if="index==0" name="arrow_drop_down"></material-icon>
        {{ pageName }}
      </a>
      <div class="navigation-item">
        <div class="search">
          <material-icon name="search" size="16px"></material-icon>
        </div>
      </div>
      <span class="bar"></span>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'endue-header',
  data () {
    return {
      main_black: '#0B1227',
      main_red: '#FD455f',
      pages: [
        'Collections',
        'About',
        'Advertise',
        'Account'
      ]
    }
  }
}
</script>

<style lang="scss">
.bar {
  height: 3px;
  position: absolute;
  top: 85%;
}

a {
  color: inherit;
  text-decoration: none;
}

header {
  position: relative;
  display: flex;
  flex-direction: row;
  width: 100vw;
}

#logo {
  background-color: white;
  width: /*10.625em*/ 9vw;
  height: /*10.625em*/ 9vw;
  color: black;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;

  span:not(.bar) {
    font-weight: bold;
    font-size: 1.5rem;
    margin-top: 1vh;
    sup {
      font-size: 0.15rem;
    }
  }

  .bar {
    background-color: black;
    width: 65%;
  }
}

nav {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  flex: 1 0 auto;

  .navigation-item {
    padding: 2vw;
    padding-bottom: 3vw;
    font-size: 0.95rem;
    display: inline-block;
  }

  .bar {
    background-color: #2D4C79;
    width: 100%;
  }

  .search {
    border: 1px solid rgba(255,255,255,0.5);
    border-radius: 100%;
    width: 24px;
    height: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 2vw;
  }
}

</style>

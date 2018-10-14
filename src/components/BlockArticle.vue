<template>
  <article :class="article.class">
    <h2>{{ article.group }}</h2>
    <span class="bar"></span>
    <div class="article-catbar">
      <h4>{{ article.category }}</h4>
      <material-icon name="favorite" v-if="article.liked"></material-icon>
    </div>
    <img v-if="article.image" :src="article.image" :alt="article.title" />
    <h1>{{ article.title }}</h1>
  </article>

</template>

<script>
export default {
  name: 'BlockArticle',
  props: ['article']
}
</script>

<style lang="scss">
article {
  width: 45%;
  min-height: 400px;
  margin: 1vw;
  position: relative;
  padding: 20px;
  overflow: hidden;
  z-index: 0;

  // stolen from https://stackoverflow.com/a/33122202/1473963

  &:after {
    height: 90%;
    bottom: 0px;
    border: 2px solid rgba(255,255,255,0.5);
    border-width: 0px 2px 2px 0px;
  }

  &:before {
    height: 10%;
    top: 0;
    border: 2px solid rgba(255,255,255,0.5);
    border-width: 2px 3px 0px 0px;
    transform: skew(45deg);
    transform-origin: right bottom;
  }

  &:after, &:before {
    position: absolute;
    content: '';
    width: calc(100% - 2px);
    left: 0px;
    z-index: -1;
  }

  h2 {
    font-weight: 100;
    font-size: 1.75rem;
    text-transform: uppercase;
    margin: 0;
    margin-bottom: 2vh;
  }

  span.bar {
    height: 3px;
    width: 50px;
    position: absolute;
  }

  .article-catbar {
    display: flex;
    justify-content: space-between;
    padding-top: 2vh;
    padding-bottom: 2vh;
    font-size: 1.15rem;

    h4 {
      margin: 0;
    }

    i.material-icons {
      color: #FD455F;
    }
  }

  img {
    width: 100%;
  }

  h1 {
    font-family: "Bodoni 72", serif;
    font-size: 2.25rem;
    margin-top: 2vh;
  }
}

.filled {
  // background-color: white;
  border-left: 2px solid white;
  color: black;

  &:after, &:before {
    background-color: white;
  }

  span.bar {
    background-color: #FD455F;
  }
}

.unfilled {
  background-color: transparent;
  border-left: 2px solid rgba(255,255,255,0.5);
  color: white;

  span.bar {
    background-color: rgba(255,255,255,0.5);
  }
}
</style>

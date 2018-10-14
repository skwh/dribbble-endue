<template>
  <div id="articles">
    <block-article v-for="(post, index) in articles" :key="`article-${index}`" :article="post"></block-article>
    <sub>MORE</sub>
  </div>
</template>
<script>
import BlockArticle from './BlockArticle'

export default {
  name: 'EndueArticles',
  components: { BlockArticle },
  data () {
    return {
      articles: [
        {
          class: 'filled',
          group: 'Oct 07',
          category: 'Daily Design Inspiration',
          liked: true,
          image: require('../assets/colors.jpg'),
          title: 'Daily Design Inspiration for Oct 07'
        },
        {
          class: 'unfilled',
          group: 'Design',
          category: 'Editorial Collection',
          liked: false,
          image: '',
          title: 'Minimalist Editorial Design for Apple'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
#articles {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-around;
  align-items: flex-start;
  margin-top: 100px;
  position: relative;

  sub {
    position: absolute;
    top: 3vh;
    right: -0.8vw;
    transform: rotate(-90deg);
    font-size: 0.5rem;
    text-transform: uppercase;
    color: rgba(255,255,255,0.5);
  }

  &:after {
    position: absolute;
    top: 6vh;
    right: 0;
    content: '';
    height: 45vh;
    width: 0px;
    border-right: 2px dotted rgba(255,255,255,0.5);
  }
}
</style>

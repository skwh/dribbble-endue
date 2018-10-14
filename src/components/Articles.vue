<template>
  <div id="articles">
    <block-article v-for="(post, index) in articles" :key="`article-${index}`" :article="post"></block-article>
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
}
</style>

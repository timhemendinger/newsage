<template>
    <div class="columns is-marginless">
      <sidebar :siteList="siteList"></sidebar>
      <article-list></article-list>
      <article-content></article-content>
    </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue';
import ArticleList from './components/ArticleList.vue';
import ArticleContent from './components/ArticleContent.vue';

export default {
  name: 'app',
  data () {
    return {
      siteList: [
        { 
          title: 'A List Apart',
          url: 'http://alistapart.com/main/feed'
         },
         {
           title: 'Smashing Magazine',
           url: 'http://rss1.smashingmagazine.com/feed/'
         }
      ]
    }
  }, 
  components: {
    sidebar: Sidebar,
    articleList: ArticleList,
    articleContent: ArticleContent
  }
}
</script>

<style>
  @import '../node_modules/bulma/css/bulma.css';
</style>

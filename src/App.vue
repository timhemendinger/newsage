<template>
    <div class="columns is-marginless">
      <sidebar :siteList="siteList"></sidebar>
      <article-list></article-list>
    </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue';
import ArticleList from './components/ArticleList.vue';

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
           url: ''
         }
      ]
    }
  }, 
  components: {
    sidebar: Sidebar,
    articleList: ArticleList
  }
}
</script>

<style>
  @import '../node_modules/bulma/css/bulma.css';
</style>

<template>
    <div class="columns is-marginless">
      <sidebar></sidebar>
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

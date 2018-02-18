<template>
  <div class="column" v-html="articleContent">
        
  </div>
</template>

<script>
import { eventBus } from '../main';

export default {
    data: function() {
        return {
            articleContent: ''
        }
    },
    created() {
        eventBus.$on('newArticleSelected', (data) => {
            this.articleContent = data;
        });
    }
}
</script>

<style scoped>
    .column {
        border-left: 1px solid #ccc;
    }
</style>

<style>
p {
    margin: 1em;
}
</style>


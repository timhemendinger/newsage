<template>

  <aside class="column is-2 hero is-fullheight menu is-paddingless">

    <ul class="menu-list">
        <li v-for="site in siteList"><a @click="retrieveRSSData(site.url)">{{ site.title }}</a></li>
    </ul>
    
</aside>

</template>

<script>
import Parser from 'rss-parser';
import { eventBus } from '../main';

export default {
  props: ['siteList'],
  data: function(){
      return {
          items: []
      }
  },
  methods: {
    retrieveRSSData(url) {
        var parseString = 'https://cors.now.sh/' + url;

        let parser = new Parser();

        (async () => {
            let feed = await parser.parseURL(parseString);

            feed.items.forEach(item => {
                this.items.push(item.title)
            });

            eventBus.$emit('newLinkSelected', this.items);
        })();
    }
  }
}
</script>


<style scoped>
    .menu {
        background-color: #004e6a;
    }

    a, a:link, a:visited {
        color: #fff;
    }

    .menu-list a:hover {
        background-color: #096981 !important;
        color: #fff;
    }

    .is-active {
        background-color: #096981 !important;
    }
</style>

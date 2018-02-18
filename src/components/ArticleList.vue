<template>

  <div class="column is-3">
      
      <div v-for="(item, index) in items" class="card" @click="newArticleSelected(index)">
            <div class="card-content">
                <div class="content">
                    {{ item.title }}
                </div>
            </div>
        </div>
  </div>

</template>

<script>
import { eventBus } from '../main';

export default {

    data: function() {
        return {
            items: null
        }
    },
    methods: {
        newArticleSelected(index) {
            eventBus.$emit('newArticleSelected', this.items[index].content);
        }
    },
    created() {
        eventBus.$on('newLinkSelected', (data) => {
            this.items = data;
        });
    }
}
</script>


<style scoped>
    .card {
        cursor: pointer;
    }

    .card:hover {
        background-color: #eee;
    }
</style>

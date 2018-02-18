<template>

  <aside class="column is-3 hero is-fullheight menu">

      <div v-for="item in items" class="card">
            <div class="card-content">
                <div class="content">
                    <strong>{{ item }}</strong>
                </div>
            </div>
        </div>
            
  </aside>

</template>

<script>
import { eventBus } from '../main';

export default {

    data: function() {
        return {
            items: null
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

</style>

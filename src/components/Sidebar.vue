<template>

  <aside class="column is-2 hero is-fullheight menu is-paddingless">

    <ul class="menu-list">
        <li><a class="is-active">A List Apart</a></li>
        <li><a>Smashing Magazine</a></li>
        <li><a>DailyJS</a></li>
        <li><a>Some Blog</a></li>
        <li><a>Another Blog</a></li>
        <li><a>Hacker News</a></li>
    </ul>
    
</aside>

</template>

<style scoped>
    aside {
       
    }

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

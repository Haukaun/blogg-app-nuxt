
<template>
    <div class="bg-mainBg">
        <NavBar />
        <NewsCollage />
    </div>
</template>

<script lang="ts">

import NavBar from '../components/navbar/NavBar.vue'
import NewsCollage from '../components/newsCollage/newsCollage.vue'
import Vue from 'vue'

export default Vue.extend({
    name: 'FrontPage',
    components: {
    NavBar,
    NewsCollage
},
})
</script>

<template>
    <div class="bg-mainBg">
        <NavBar />
    </div>
</template>

<script lang="ts">

import NavBar from '../components/navbar/NavBar.vue'
import Vue from 'vue'

export default Vue.extend({
    name: 'Indexpage',
    components: {
    NavBar
},
})
</script>
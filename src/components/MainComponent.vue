<template>
    <div class="main">
        <SongsList/>
    </div>
</template>

<script>
import SongsList from './SongsList.vue'

export default {
    name: 'MainComponent',
    components: {
        SongsList
    }
}
</script>

<style lang="scss" scoped>
    @import '../scss/variables.scss';
    
    .main {
        height: 100vh;
        background-color: $_secondaryColor;
    }
</style>
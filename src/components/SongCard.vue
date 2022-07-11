<template>
    <div class="card text-center">
        <img :src="album.poster" :alt="album.title">
        <h5>{{ album.title }}</h5>
        <div class="author-name">{{ album.author }}</div>
        <div class="description">{{ album.year }}</div>
    </div>
</template>

<script>
export default {
    name: 'SongCard',
    props: {
        album: Object
    }
}
</script>

<style lang="scss" scoped>
    @import '../scss/variables.scss';
    .card {
        background-color: $_primaryColor;
        height: 100%;

        img {
            margin: 10px;
        }

        h5 {
            color: white;
        }
        .author-name {
            color: gray;
        }
        .description {
            color: gray;
            margin-bottom: 10px;
        }
    }
</style>
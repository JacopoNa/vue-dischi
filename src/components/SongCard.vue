<template>
    <div class="card text-center">
        <img :src="album.poster" :alt="album.title">
        <h3>{{ album.title }}</h3>
        <div class="description">{{ album.author }}</div>
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

        img {
            margin: 10px;
        }

        h3 {
            color: white;
        }
        .description {
            color: gray;
        }
    }
</style>
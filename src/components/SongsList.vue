<template>
    <div class="list">
        <div class="row row-cols-5">
            <div class="col" v-for="(element,index) in listOfSongs" :key="index">
                <SongCard :album="element"/>
            </div>

        </div>
    </div>
</template>

<script>
import axios from "axios";
import SongCard from './SongCard.vue'

export default {
    name: 'SongsList',
    components: {
        SongCard
    },
    data() {
        return {
            url: "https://flynn.boolean.careers/exercises/api/array/music",
            listOfSongs: []
        }
    },
    created() {
        this.getSongs()
    },
    methods: {
        getSongs() {
            axios.get(this.url).then((result)=> {
            this.listOfSongs = result.data.response
            })
        }
    }
}
</script>

<style lang="scss" scoped>
    .list {
        width: 60%;
        margin: 0 auto;
        padding-top: 70px;
    }
</style>
<template>
    <div class="card">
        <img :src="spotifyData.poster" alt="">
        <span class="album_title">{{spotifyData.title}}</span>
        <span class="album_author">{{spotifyData.author}}</span>
        <span class="album_year" >{{spotifyData.year}}</span>
    </div>
</template>

<script>
export default {
    name:'MainContent',
    props:{
        spotifyData : Object
    }
}
</script>

<style lang="scss" scoped>

</style>
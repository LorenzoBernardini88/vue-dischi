<template>
    <div class="card">
        <img :src="spotify.poster" :alt="spotify.name">
        <span class="album_title">{{spotify.title}}</span>
        <span class="album_author">{{spotify.author}}</span>
        <span class="album_year" >{{spotify.year}}</span>
    </div>
</template>

<script>
export default {
    name:'MainContent',
    props:{
        spotify : Object
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
    .card{
        text-align: center;
        background: $color3;
        padding: 10px 10px 0 10px;
    }
</style>
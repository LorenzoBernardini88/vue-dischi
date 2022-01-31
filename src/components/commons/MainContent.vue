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
        width: 150px;
        padding: 10px 10px 30px 10px;
        display: flex;
        flex-direction: column;
        align-items: center;
        img{
            width: 90%;
        }
    }   .album_title{
        margin-top: 10px;
        color:#FCF1DB;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 15px;
        }
        .album_author{
            margin-top:10px;
        }
        .album_author,
        .album_year{
            color: #6B7F7D;
            font-size: 12px;
        }
</style>
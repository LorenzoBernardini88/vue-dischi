<template>
    <div class="logo_cont">
        <img src="../../assets/img/spotify_logo.png" alt="">
    </div>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.logo_cont {
    background: $color2;
    padding: 5px 10px;
    img{
        height: 50px;
        width: 50px;
        
    }
}

</style>
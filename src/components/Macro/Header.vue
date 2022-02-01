
<template>
    <header class="head_cont">
        <div class="logo_cont">

        <img src="../../assets/img/spotify_logo.png" alt="">
        </div>
        
    </header>
</template>
    
    


<script>

export default {
    name: 'Header',
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.head_cont {
    background: $color2;
    padding: 5px 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    
        img{
            height: 50px;
            width: 50px;
        }
    
}
</style>
        
        
        

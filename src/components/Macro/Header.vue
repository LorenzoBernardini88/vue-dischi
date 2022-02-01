
<template>
    <header class="head_cont">
        <div class="logo_cont">

        <img src="../../assets/img/spotify_logo.png" alt="">
        </div>
        <Select/>
    </header>
</template>
    
    


<script>
import Select from '../commons/Select.vue';
export default {
    name: 'Header',
    data() {
        return{
            apiURL : "https://flynn.boolean.careers/exercises/api/array/music",
            
            
        }
    },
    components:{
        Select
    }
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
        
        
        

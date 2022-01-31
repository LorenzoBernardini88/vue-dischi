<template>
    <div class="container">
        <MainContent/>
    </div>
</template>

<script>
import MainContent from '../commons/MainContent.vue'
export default {
    name:'Main',
    components:{
        MainContent
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.container{
    display: flex;
    flex-wrap: wrap;
}
</style>
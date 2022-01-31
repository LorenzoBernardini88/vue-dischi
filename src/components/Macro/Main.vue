<template>
    <div class="container">
        <MainContent 
        v-for="(album,indice) in cardArray"
        :key="indice"
        :spotify="album"/>
    </div>
</template>

<script>
import axios from "axios";
import MainContent from '../commons/MainContent.vue';
export default {
    name:'Main',
    data() {
        return{
            apiURL : "https://flynn.boolean.careers/exercises/api/array/music",
            cardArray: [],
        }
    },
    components:{
        MainContent
    },
    created(){
        this.getCards();
    },
    methods:{
        getCards(){
            axios
                .get(this.apiURL)
                .then( (risposta) => {
                    // handle success
                    this.cardArray = risposta.data.response;
                })
                .catch(function (error) {
                    // handle error
                    console.log(error);
                });
        }
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
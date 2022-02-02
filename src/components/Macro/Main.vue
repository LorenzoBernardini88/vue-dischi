<template>
    <div class="general" >
        <Select :generi="arrayGeneri"
            @seleziona = "filtraAlbum"/>
        <div v-if="!loading" class="container">
            <MainContent 
            v-for="(album,indice) in albumFiltrati"
            :key="indice"
            :spotify="album"/>
        </div>
        <Loader v-else />
    </div>
</template>


<script>
import axios from "axios";
import MainContent from '../commons/MainContent.vue';
import Loader from "../commons/Loader.vue";
import Select from '../commons/Select.vue';
export default {
    name:'Main',
    data() {
        return{
            apiURL : "https://flynn.boolean.careers/exercises/api/array/music",
            cardArray: [],
            loading : true,
            selectGenre:"",
            arrayGeneri: []
        }
    },
    components:{
        MainContent,
        Loader,
        Select
    },
    created(){
        this.getCards();
    },
    computed:{
        albumFiltrati(){            

            if( this.selectGenre == 'All' ){
                return this.cardArray 
                } 
                
            return this.cardArray.filter( (cover) => {                
                return cover.genre.includes(this.selectGenre);
            });

        }
    },
    methods:{
        getCards(){
            axios
                .get(this.apiURL)
                .then( (risposta) => {
                    // handle success
                    this.cardArray = risposta.data.response;
                    this.filtraGeneri()
                    this.loading = false;
                    
                })
                .catch(function (error) {
                    // handle error
                    console.log(error);
                });
        },
        filtraAlbum(inputSelect){
            this.selectGenre = inputSelect;
            console.log(inputSelect);
        },
        filtraGeneri(){
            this.cardArray.forEach((elemento)=>{
                if(!this.arrayGeneri.includes(elemento.genre)){
                    this.arrayGeneri.push(elemento.genre);
                }
            });
        }
    },
    mounted: function(){
        console.log(this.filtraGeneri);
    }
}


</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.general{
    text-align: center;
}
.container{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 20px 30px;
    padding: 50px 0;
}
</style>
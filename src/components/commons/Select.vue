<template>
    <div class="slc_cont">
        <span class="select_name">Seleziona Genere</span>
        <select v-model="option" @change="$emit('seleziona',option)">
            <option value="">All</option>
            <option v-for="(elemento,indice) in generi" :key="indice" :value="elemento">{{elemento}}</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'Select',
    props:{
        generi: Array,
    },
    data() {
        return{
            option: "",
            //arrayProva:[]
        }
    },
    // methods:{
    //     clonaGeneri:function(){
    //         this.arrayProva = this.generi;
    //     }
    // },
    // watch:{
    //     generi: function(){
    //         console.log('ciao');
    //         this.clonaGeneri();
            
    //     }
    // }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
.slc_cont{
    margin-top:20px;
    span{
    text-transform: uppercase;
    font-size:15px;
    font-weight:200;
    margin-right: 5px;
    color:lightgray;
    }
    select{
        background:$color3;
        border:none;
        color:lightgray;
    }
} 
    
</style>
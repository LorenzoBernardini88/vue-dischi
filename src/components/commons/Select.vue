<template>
    <div class="slc_cont">
        <span class="select_name">Seleziona Genere</span>
        <select v-model="option" @change="$emit('seleziona',option)">
            <option value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'Select',
    data() {
        return{
            option: ""
        }
    }
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
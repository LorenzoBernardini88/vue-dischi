<template>
    <div class="slc_cont">
        <select v-model="option" @change="$emit('seleziona',option)">
            <option value=""></option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
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
</style>
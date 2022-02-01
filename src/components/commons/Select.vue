<template>
    <div class="slc_cont">
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
</style>
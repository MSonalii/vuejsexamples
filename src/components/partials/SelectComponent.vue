<template>
    <div class="field">
        <div class="control">
            <div class="select is-primary">
                <select>
                    <option v-for="(cat,index) in categary" :key="index">{{cat}}</option> 
                </select>
            </div>
        </div>
    </div>
</template>
<script>
const SelectComponent = {
    name:'select-component',
    props: ['categary'],
        data(){
        return{

        }
    }
}
export default SelectComponent
</script>

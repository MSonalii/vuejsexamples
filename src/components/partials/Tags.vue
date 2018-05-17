<template>
<span>
 <div class="tags" >
    <span v-for="(tag,index) in tags" :key="index" class="tag is-info">{{tag}}  
        <button class="delete is-small"></button>
    </span>     
</div>
</span>
</template>
<style lang="scss" scoped>
    .tags{
        margin-bottom: 10px;
    }
</style>

<script>
const Tags = {
    name:'tag-component',
    props:['tags'],
    data(){
        return{

        }
    }
}
export default Tags
</script>

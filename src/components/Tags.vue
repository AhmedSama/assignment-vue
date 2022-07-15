<template>
     <div class="flex align-center gap mb">
        <div class="tag" v-for="tag in tags" :key="tag">{{tag}}</div>
     </div>
</template>

<script>
    export default {
        props:{
            tags : Array
        }
    }
</script>

<style scoped>

    .tag{
        background-color: #B03337;
        color: white;
        font-size: 10px;
        padding: 3px 6px;
    }
    
</style>

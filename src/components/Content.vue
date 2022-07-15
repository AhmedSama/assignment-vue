<template>
    <p className="article mb-1">{{text}}</p>
</template>

<script>
export default {
    props:{
        text : String
    }
}
</script>
<style scoped>
    .article{
        font-size: 15px;
        font-weight: 400;
    }
</style>
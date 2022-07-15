<template>
     <div class="img-container mb-2">
        <img v-if="image" :src="image" alt="article image">
        <img v-else src="../assets/images/image.png" alt="placeholder image">
     </div>
</template>

<script>
    export default{
        props:{
            image : String
        }
    }
</script>


<style scoped>
    .img-container{
    width: 100%;
    overflow: hidden;
    /* center the image inside it */
    display: grid;
    place-items: center;
    object-fit: cover;
    }
    img{
    width: 100%;
    height: 100%;
    }
</style>
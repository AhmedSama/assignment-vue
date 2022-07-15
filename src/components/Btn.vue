<template>
     <div @click="clickevent" class="rounded-btn" :class="[(className!==null,className)]">
        <slot></slot>
     </div>
</template>

<script>
    export default{
        props:{
            clickevent : Function,
            className : String
        }
    }
</script>
<style scoped>
    .rounded-btn{
        padding: 5px 10px;
        font-size: 15px;
        background-color: rgb(243, 243, 243);
        width: 100%;
        height: 100%;
        color: rgb(56, 56, 56);
        cursor: pointer;
        white-space: nowrap;
        transition: 0.2s all ease;
    }
    .rounded-btn:hover,.rounded-btn.active{
        background-color: rgb(225, 225, 225);
    }
</style>
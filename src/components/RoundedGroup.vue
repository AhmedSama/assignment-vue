<template>
    <div className='rounded-group'>
        <slot></slot>
    </div>
</template>

<script>
    export default{
        
    }
</script>
<style scoped>
    .rounded-group{
        background-color: rgb(243, 243, 243);
        border-radius: 1000px;
        display: flex;
        align-items: center;
        overflow: hidden; 
    }
</style>
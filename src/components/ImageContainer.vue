<script setup>    
    defineProps(['image']);
</script>

<template>
    <div id="image-container">        
        <img :src="image.src" class="img-thumbnail">    
    </div>
</template>

<style scoped>
#image-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-grow: 1;
    overflow: hidden;
    padding: 15px;
}

img {
    max-width: 200px;
    max-height: 150px;
}
</style>
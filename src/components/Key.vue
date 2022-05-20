<script setup>
    defineProps(['dataKey','details']);


</script>

<template>
    <button class="singleButton" :data-key="dataKey">{{details}}</button>    
</template>

<style scoped>

#singleButton {
    font-family: inherit;
    font-weight: bold;
    border: 0;
    padding: 0;
    height: 50px;
    cursor: pointer;
    background-color: rgb(129, 131, 132);
    color: rgb(215, 218, 220);
    flex-grow: 1;
    text-transform: uppercase;
    margin-right: 6px;
    border-radius: 4px;
    user-select: none;
}

</style>
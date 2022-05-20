<script setup>

import Key from './Key.vue';

const row1Keys = ['q','w','e','r','t','y','u','i','o','p'];
const row2Keys = ['a','s','d','f','g','h','j','k','l'];
const row3Keys = ['z','x','c','v','b','n','m'];

</script>

<template>

    <div id="keyboard-container">
        <div class="keyboard-row">
            <Key v-for="(row1Key,index) in row1Keys" :key="row1Key" :data-key="row1Key" :details="row1Key" @click="$emit('buttonPressed',row1Key)"></Key>
        </div>

        <div class="keyboard-row">
            <div class="spacer-half"></div>
            <Key v-for="(row2Key,index) in row2Keys" :key="row2Key" :data-key="row2Key" :details="row2Key" @click="$emit('buttonPressed',row2Key)"></Key>
            <div class="spacer-half"></div>
        </div>

        <div class="keyboard-row">
            <Key :data-key="'enter'" class="'wide-button'" :details="'Enter'" @click="$emit('buttonPressed','Enter')"></Key>            
            <Key v-for="(row3Key,index) in row3Keys" :key="row3Key" :data-key="row3Key" :details="row3Key" @click="$emit('buttonPressed',row3Key)"></Key>
            <Key :data-key="'del'" class="'wide-button'" :details="'Del'" @click="$emit('buttonPressed','Del')"></Key>            
        </div>
    </div>
    
</template>

<style scoped>
#keyboard-container {
    height: 175px;
    margin: 0.5em;
}

.keyboard-row {
    display: flex;
    justify-content: center;
    width: 100%;
    margin: 0 auto 8px;
    touch-action: manipulation;
}

.keyboard-row button {
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

.keyboard-row button.wide-button {
    flex-grow: 1.5;
}

.spacer-half {
    flex-grow: 1.5;
}
</style>
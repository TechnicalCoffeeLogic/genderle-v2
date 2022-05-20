<script setup>

import { inject } from 'vue';
import GameSquare from './GameSquare.vue';

const props = defineProps(['wordLength','numberOfTries']);
let squares = createSquares(props.wordLength, props.numberOfTries);

/** 
** --------------------------------------------------------------
** purpose: create the squares for the game
** pass...: max length of the word for the game, number of tries
** return.: array of number of squares to look over
** -------------------------------------------------------------- */
function createSquares(wordLength, numberOfTries) {

    let squares = [];
    for (let index = 0; index < (wordLength * numberOfTries); index++) {
        squares[index] = index;
    }

    return squares;
};

</script>

<template>
    <div id="board-container">
        <div id="board">
            <GameSquare v-for="(square, index) in squares" :id="index + 1" :key="index + 1"></GameSquare>
        </div>
    </div>
</template>

<style>
#board-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-grow: 1;
    overflow: hidden;
}

#board {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    grid-gap: 5px;
    padding: 10px;
    box-sizing: border-box;
}
</style>

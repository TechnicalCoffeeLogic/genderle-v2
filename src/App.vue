<script setup>

import HeaderNav from './components/HeaderNav.vue'

</script>

<template>
  <div id="game">
    <HeaderNav></HeaderNav>
  </div>
</template>

<style>
#app {
    display: flex;
    background-color: rgb(19,21,25);
    height: 100%;
    align-items: center;
    flex-direction: column;
}

#game {
    width: 100%;
    max-width: 500px;
    height: 100%;
    display: flex;
    flex-direction: column;
}
</style>

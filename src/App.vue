<script setup>

import {ref} from 'vue'
import HeaderNav from './components/HeaderNav.vue'
import ImageContainer from './components/ImageContainer.vue'

const image = ref({src: "", word: ""});

// -------------------------------------------------------------------------------------------------------------------------------
// purpose: setup image and word
// pass...: nothing
// return.: nothing
// -------------------------------------------------------------------------------------------------------------------------------
function setImage() {
  const numberOfPics = 12;
  const imageObject = [
    {
      src: "./public/images/man1.jpg",
      word: "male  "
    },
    {
      src: "./public/images/man2.jpg",
      word: "male  "
    },
    {
      src: "./public/images/woman1.jpg",
      word: "female"
    },
    {
      src: "./public/images/man3.jpg",
      word: "male  "
    },
    {
      src: "./public/images/woman2.jpg",
      word: "female"
    },
    {
      src: "./public/images/woman3.jpg",
      word: "female"
    },
    {
      src: "./public/images/man4.jpg",
      word: "male  "
    },
    {
      src: "./public/images/man5.jpg",
      word: "male  "
    },
    {
      src: "./public/images/man6.jpg",
      word: "male  "
    },
    {
      src: "./public/images/man7.jpg",
      word: "male  "
    },
    {
      src: "./public/images/woman4.jpg",
      word: "female"
    },
    {
      src: "./public/images/woman5.jpg",
      word: "female"
    }
  ]

  let newDate = new Date();
  let picIndex = newDate.getDate() % numberOfPics;
  image.src = imageObject[picIndex].src;
  // tmpWord = word;
  // word = imageObject[picIndex].word;    
  return image;
}

</script>

<template>
  <div id="game">
    <HeaderNav></HeaderNav>
    <ImageContainer :image="setImage()"></ImageContainer>
  </div>
</template>

<style>
#app {
  display: flex;
  background-color: rgb(19, 21, 25);
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

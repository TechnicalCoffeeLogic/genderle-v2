<script setup>

import {ref} from 'vue'
import MenuModal from './MenuModal.vue'
import HowToPlayModal from './HowToPlayModal.vue'

// reactive state
const visibility = ref(false);

defineProps({});

</script>

<template>
    <header>
        <ul class="nav">
            <li>
                <div>
                    <h1 class="title display-1">GENDERLE</h1>
                </div>
            </li>
            <li class="nav-item">
                <div>
                    <a type="button" class="nav-link active" data-bs-toggle="modal" data-bs-target="#helpModal"
                        aria-current="page" href="#" @click="showModal">
                        <i class="bi bi-question-circle"></i>
                    </a>
                </div>
            </li>
        </ul>
    </header>

    <HowToPlayModal :isVisible="this.visibility"></HowToPlayModal>
    <MenuModal></MenuModal>

</template>

<style scoped>
a {
    color: #42b983;
}

header{
    border-bottom: 1px solid rgb(58,58,60);
}

.title {
    color: gainsboro;
    font-size: 2.5rem;
    font-weight: bold;
    margin: .4rem 0 .4rem 0;
    text-align: center;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 
    'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

.nav {
    align-items: center;
    justify-content: center;
}

#help-icon {
    color: gainsboro;
    font-size: 1.5rem;
    text-align: right;   
    margin: .4rem 0 .4rem 0;
}
</style>

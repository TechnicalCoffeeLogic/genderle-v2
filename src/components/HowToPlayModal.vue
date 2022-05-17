<script setup>

import { onMounted } from 'vue'

const props = defineProps(['isVisible']);

// when app has been loaded show the 'how to play' modal
onMounted(() => {
    showHowToPlayModal();
    console.log('onMounted');
})

// -------------------------------------------------------------------------------------------------------------------------------
// purpose: shows user the 'how to play modal' when they visit the website
// pass...: nothing
// return.: nothing
// -------------------------------------------------------------------------------------------------------------------------------
function showHowToPlayModal() {

    var options = { backdrop: true, keyboard: false, focus: true };
    var myModal = new bootstrap.Modal(document.getElementById('howToModal'), options);
    myModal.show();
}

</script>

<template>

    <div class="modal fade" tabindex="-1" id="howToModal">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="modalTitle"><strong>How To Play</strong></h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body" id="howToModalBody">
                    Determine the correct gender of the person in the picture that is presented to you. You will get
                    five tries to figure out the correct gender, your guess can have blank spaces in them, that means
                    you do not have to fill out the entire 6 squares. <br /><br />
                    <ul>
                        <li>
                            <i class="bi bi-square-fill" style="color:rgb(83,141, 78);"></i> A green square means you
                            have the correct letter in the correct position.
                        </li>
                        <li>
                            <i class="bi bi-square-fill" style="color:rgb(181, 159, 59);"></i> A yellow square means you
                            have the correct letter, but in the wrong postition of the word.
                        </li>
                        <li>
                            <i class="bi bi-square-fill" style="color:rgb(58, 58, 60);"></i> A gray sqaure means that
                            the letter does not exist in the answer.
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

</template>

<style scoped>
.nav-item {
    display: flex;
    margin-right: 1rem
}

ul {
    list-style: none;
}
</style>
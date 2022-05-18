<script setup>

    // -------------------------------------------------------------------------------------------------------------------------------
    // purpose: Show alert message
    // pass...: message to display, type of alert
    // return.: nothing
    // -------------------------------------------------------------------------------------------------------------------------------    
    function alert(message, type) {

      var alertPlaceholder = document.getElementById('modalBody')
      var wrapper = document.createElement('div')      
      wrapper.innerHTML = '<div class="alert alert-' + type + ' role="alert">' + message + '</div>'
      alertPlaceholder.append(wrapper)

      var modalTitle = document.getElementById('modalStatusTitle');
      if (type === 'success'){
        modalTitle.innerText = 'Success';
      }
      else {
        modalTitle.innerText = 'Failed';
      }

      var options = {backdrop: true, keyboard: false, focus: true};
      var myModal = new bootstrap.Modal(document.getElementById('statusModal'), options);

      myModal.show();
      console.log(myModal);
    }

</script>

<template>
    <div class="modal fade" tabindex="-1" id="statusModal">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="modalStatusTitle"></h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body" id="modalBody">
                    <!-- this is where the alert is going -->
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
</style>
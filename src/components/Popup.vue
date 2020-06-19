<template>
    
<div>
  <b-button id="show-btn" @click="$bvModal.show('bv-modal-example')">Open Form</b-button>

  <b-modal id="bv-modal-example" hide-footer>
    <template v-slot:modal-title>
      Form Detail
    </template>
    <div class="d-block text-center">
      <form>
  <div class="form-row">
    <div class="form-group col-md-6">
      <label for="inputEmail4">text</label>
      <input type="text" class="form-control" id="inputEmail4">
    </div>
    <div class="form-group col-md-6">
      <label for="inputPassword4">Text</label>
      <input type="text" class="form-control" id="inputPassword4">
    </div>
  </div>
  <div class="form-group">
    <label for="inputAddress">Address</label>
    <input type="text" class="form-control" id="inputAddress" placeholder="1234 Main St">
  </div>
  <div class="form-group">
    <label for="inputAddress2">Address 2</label>
    <input type="text" class="form-control" id="inputAddress2" placeholder="Apartment, studio, or floor">
  </div>
  
  <div class="form-group">
    <div class="form-check">
      <input class="form-check-input" type="checkbox" id="gridCheck">
      <label class="form-check-label" for="gridCheck">
        Check me out
      </label>
    </div>
  </div>
  <button type="submit" class="btn btn-primary">Sign in</button>
</form>
    </div>
    <b-button class="mt-3" block @click="$bvModal.hide('bv-modal-example')">Close Me</b-button>
  </b-modal>
</div>





</template>

<script>
export default {
    name: "Popup",
  components: {}
}
</script>

<style scoped>

</style>
<template>
 <div class="container">
    <div class="d-table">
      <div class="row">
         <div class="col-12">
            <table class="table table-striped table-inverse">
  <thead>
    <tr>
      <th>#</th>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Username</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>Larry</td>
      <td>the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
</table>
<div class="dtb-next">
  <b-button-toolbar key-nav aria-label="Toolbar with button groups">
    <b-button-group class="mx-1">
     <b-button>&lsaquo;</b-button>
      <b-button>&rsaquo;</b-button>
    </b-button-group>
  </b-button-toolbar>
</div>
         </div>


      </div>
    </div>
 </div>
</template>

<script>
export default {
    name: "Table",
  components: {}
}
</script>

<style scoped>
.d-table{
  border:1px solid #000;
  border-radius: 5px;
  padding: 10px;
}
</style>
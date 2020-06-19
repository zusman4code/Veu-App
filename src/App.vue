<template>
  <div id="app">
  <Header />
  <div class="container-fluid cf-sprt">
    <router-view/>
  </div>
  <Popup />
  <Table />
  <Form />
  <Customers />
  <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue"; 
import Customers from "@/components/Customers.vue";
import Table from "@/components/Table.vue";
import Popup from "@/components/Popup.vue"; 
import Form from "@/components/Form.vue";


export default {
 components:{
   Header,
   Footer,
   Customers,
   Table,
   Popup,
   Form
 }
  
}
</script>
.navbar{
  background:black;

}



<style>
.cf-sprt{
padding:0px !important;
margin-top:90px;
}
</style>

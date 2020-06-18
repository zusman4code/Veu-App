<template>
  <div id="app">
  <Header />
  <div class="container-fluid cf-sprt">
    <router-view/>
  </div>
  <Customers />
  <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue"; 
import Customers from "@/components/Customers.vue";
export default {
 components:{
   Header,
   Footer,
   Customers
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

<template>
  <div>
    <my-header></my-header>
    <div class="container">
      <products></products>
      <product-details></product-details>
    </div>
  </div>
</template>

<script>
  import myHeader from './Header.vue';
  import ProductList from './ProductsList.vue';
  import ProductDetails from './ProductDetails.vue';

  export default {
    data() {
      return {
      }
    },
    components: {
      myHeader,
      'products': ProductList,
      ProductDetails
    },
  }
</script>

<style>
 .container{
   display:flex;
   align-items: flex-start;
 }
</style>

<template>
  <div>
    <my-header>
      <h1>Communication between components in Vue.js</h1>
      <span>{{secondPart}}</span>
      <h2 slot="subtitle">Slots</h2>
      <span slot="subtitle">Slots Second Part</span>
    </my-header>
    <div class="container">
      <products></products>
      <product-details></product-details>
      <product-add></product-add>
    </div>
  </div>
</template>

<script>
  import myHeader from './Header.vue';
  import ProductList from './ProductsList.vue';
  import ProductDetails from './ProductDetails.vue';
  import ProductAdd from './ProductAdd';

  export default {
    data() {
      return {
        secondPart: 'Second Part',
        mode: "view"
      }
    },
    components: {
      myHeader,
      'products': ProductList,
      ProductDetails,
      ProductAdd,
    },
  }
</script>

<style>
 .container{
   display:flex;
   align-items: flex-start;
 }

  h2{
    color:red;
  }
</style>

<template>
  <div>
    <my-header>
      <h1>Communication between components in vue.js</h1>
      <h2 slot="subtitle">Slots</h2>
      <span>Second part</span>
      <span slot="subtitle">Slots - second part</span>
    </my-header>
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
        secondPart: 'Second Part'
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

  h2{
    color:red;
  }
</style>

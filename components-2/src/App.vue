<template>
  <div>
    <my-header></my-header>
    <div class="container">
      <products @viewDetailsFromList="viewDetails"></products>
      <product-details v-bind:product="selectedProduct"></product-details>
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
        selectedProduct: {}
      }
    },
    components: {
      myHeader,
      'products': ProductList,
      ProductDetails
    },
    methods: {
      viewDetails(product) {
        this.selectedProduct = product;
      }
    }
  }
</script>

<style>

</style>

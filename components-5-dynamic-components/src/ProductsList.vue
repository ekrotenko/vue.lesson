<template>
  <div>
    <product-item v-for="(product, i) in products"
                  v-bind:key="product.id"
                  v-bind:product="product"
                  v-bind:index="(i+1)">
      <!--v-on:viewDetails="viewDetails"-->

    </product-item>
  </div>
</template>

<script>
  import ProductItem from './ProductItem.vue';
  import ProductService from './ProductService';

  export default {
    data() {
      return {
        products:[]
      }
    },
    components: {
      ProductItem
    },
    created(){
      this.products = ProductService.products;
    }
  }
</script>

<template>
    <div class="product">
      <form>
        <div class="form-group">
          <label for="title">Title</label>
          <input type="text" class="form-control" id="title" placeholder="Enter title" v-model="product.title">
        </div>
        <div class="form-group">
          <label for="price">Price</label>
          <input type="text" class="form-control" id="price" placeholder="Enter price" v-model="product.price">
        </div>
        <div class="form-group">
          <label for="qt">Title</label>
          <input type="text" class="form-control" id="qt" placeholder="Enter quantity" v-model="product.qt">
        </div>
        <button type="submit" class="btn btn-primary" v-on:click.prevent="addProduct">Submit</button>
      </form>
    </div>
</template>

<script>
  import ProductService from './ProductService'

  export default {
    name: "ProductAdd",
    data(){
      return{
        product:{}
      }
    },
    methods:{
      addProduct(){
        ProductService.addProduct(this.product.title, this.product.price, this.product.qt);
      }
    }
  }
</script>

<style scoped>
  .product{
    width: 500px;
    border: 1px solid red;
    border-radius: 10px;
    margin: 10px;
    padding:10px;
  }
</style>

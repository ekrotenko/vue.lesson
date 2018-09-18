<template>
  <div>
    <h1>Hello, {{name}}</h1>
    <button v-on:click="changeName">Not {{name}}?</button>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        name: 'Eugene'
      }
    },
    methods: {
      changeName() {
        this.name = this.name === 'Eugene' ? 'Liza' : 'Eugene';
      }
    },
  }
</script>

<style>

</style>

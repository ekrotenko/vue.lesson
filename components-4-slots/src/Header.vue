<template>
  <div>
    <div>
      <slot></slot>
    </div>
    <div>
      <slot name="subtitle">Default subtitle</slot>
    </div>
    <div>
      <slot name="copyright">Eugene K, Inc.</slot>
    </div>
  </div>

</template>

<script>
  export default {

  }
</script>

<style scoped>
  div {
    text-align: center;
  }
  h2{
    color:green;
  }
</style>

<template>
  <div>
    <my-header></my-header>
    <div>

      <greetings></greetings>
      <greetings></greetings>
      <greetings></greetings>
    </div>
  </div>
</template>

<script>
  import Greetings from './Greetings.vue';
  import Header from './Header.vue';

  export default {
    components: {
      Greetings,
      'my-header': Header
    }
  }
</script>

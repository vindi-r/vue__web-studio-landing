<template lang="pug">
  span.divider
</template>

<script>
export default {
   name: 'Divider'
}
</script>

<style lang="scss">
  @import '../assets/style/vars';

  .divider {
    display: block;
    margin: 2rem 0 3rem;
    height: 1px;
    width: 1.5rem;
    background-color: $c-main;
  }
</style>
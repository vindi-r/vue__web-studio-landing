<template>
  <button class="button"></button>
</template>

<script>

export default {
  name: 'Button'
}
</script>

<style lang="scss">

  @import '../assets/style/vars';

  .button {
    box-sizing: border-box;
    min-width: 150px;
    padding: 1rem 2rem;
    border: 2px solid $c-main;
    
    background-color: transparent;
    color: $c-main;
    font-size: .8em;
    letter-spacing: .1em;
    text-align: center;
    text-transform: uppercase;
    

    cursor: pointer;
    outline: none;
  }
</style>
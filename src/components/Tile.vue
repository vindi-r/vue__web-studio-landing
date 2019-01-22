<template lang="pug">
  .tile
    .tile__content
      slot
</template>

<script>
export default {
  name: "Tile"
}
</script>

<style lang="scss">
  @import '../assets/style/vars';

  .tiles {
    grid-column: 1 / 3;
    grid-row: 1 / 2;
    justify-self: end;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: .5rem;

    
    transform: rotate(45deg);
    transform-origin: center center;

    @include bp($xxl) {
      transform: rotate(45deg) translateX(-15%) translateY(15%);
    }

    @include bp($xxxl) {
      transform: rotate(45deg) translateX(-35%) translateY(25%);
      grid-template-columns: 1fr 1fr 1fr
    }
  }

  .tile {
    width: 180px;
    height: 180px;

    background-color: $c-main;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    
    &:nth-child(1) {
      grid-column-start: 2;
    }    
    &:nth-child(2) {
      grid-column-start: 1;
    }
    &:nth-child(5) {
      grid-column-start: 2;
    }
    &:nth-child(8) {
      grid-column-start: 3;
    }

    @include bp($xxxl) {
      &:nth-child(1) {
        grid-column-start: 3;
      }
      &:nth-child(2) {
        grid-column-start: 2;
      }
      &:nth-child(6) {
        grid-column-start: 1;
      }
      &:nth-child(8) {
        grid-column-start: 1;
      }
    }


    &__content {
      transform: rotate(-45deg);
    }
    
    &__title {
      color: $c-secondary;
      text-transform: uppercase;
      font-size: .7em;
      font-weight: bold;
    }
  }
</style>



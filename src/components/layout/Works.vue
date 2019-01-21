<template lang="pug">
  section.works
    .inner.works__inner
      .wrapper
        h1.works__title Our works
        Divider.divider_black
      p.works__description
        |Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
        br
        |Aenean tincidunt sit amet at.
</template>

<script>

import Divider from '../Divider';

export default {
  name: 'Works',
  components: {
    Divider
  }
}
</script>

<style lang="scss">
  @import '../../assets/style/vars';

  .works {
    display: grid;
    grid-template-columns: 1fr 1200px 1fr;
    height: 300px;
    align-items: center;

    & * {
      margin-bottom: 0;
    }

    &__inner {
      display: grid;
      grid-template-columns: 1fr 1fr;
    }

    &__title {
      color: $c-secondary;
      text-transform: uppercase;
      font-weight: bold;
    }

    &__description {
      // to align with title
      margin-top: .5rem;

      color: $c-third;
    }
  }
</style>

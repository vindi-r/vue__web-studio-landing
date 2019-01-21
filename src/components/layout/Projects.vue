<template lang="pug">
  section.projects
    .inner.projects__inner
      .wrapper
        h1.projects__title Project title here
        Divider
        p.projects__description.
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
          Donec in leo turpis. Praesent tempus felis diam, in 
          suscipit lectus euismod et. Pellentesque habitant morbi 
          tristique senectus fames ac turpis egestas.

        Button(v-text="title")

      .check
</template>

<script>
import Button from '../Button';
import Divider from '../Divider';

export default {
  name: 'Projects',

  data: () => ({
    title: 'see it live'
  }),

  components: {
    Button,
    Divider
  }
}
</script>

<style lang="scss">
  @import '../../assets/style/vars';

  .projects {
    display: grid;
    grid-template-columns: 1fr 1200px 1fr;
    align-items: center;
    height: 900px;

    background-color: $c-secondary;
    color: $c-main;

    &__inner {
      display: grid;
      grid-template-columns: auto 1fr auto;
    }

    &__title {
      text-transform: capitalize;
      font-weight: bold;
    }

    &__description {
      margin-bottom: 4rem;
    }
  }
</style>



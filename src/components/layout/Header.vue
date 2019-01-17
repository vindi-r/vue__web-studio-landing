<template lang="pug">
  header.header
    .inner.header__inner
      .logo
        Briefcase
        p.logo__text Logo goes here
        
      .wrapper
        h1
          |So begins a new age 
          br
          |of knowledge
        p
          |Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vitae nulla quis 
          br
          |turpis cursus pharetra. Fusce blandit nec tortor sit amet ullamcorper.

        Divider
        Button(v-text='title')
</template>

<script>


import Briefcase from '../icons/Briefcase.vue';
import Divider from '../Divider.vue';
import Button from '../Button.vue';

export default {
  name: 'Header',

  data: () => ({
    title: 'projects'
  }),

  components: {
    Briefcase,
    Divider,
    Button
  }

}
</script>

<style lang="scss">

  @import '../../assets/style/vars';

  .header {
    display: grid;
    grid-template-columns: 1fr 1200px 1fr;
    height: 100vh;
    max-height: 900px;
    color: $c-main;

    /* for ::before */
    position: relative;

    &::before {
      content: '';
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;

      background-image: url('../../assets/img/banner.png');
      background-size: cover;
      background-position: center center;
      filter: brightness(60%)
    }

    &__inner {
      grid-column: 2 / 3;
      display: grid;
      align-items: center;
      grid-template-rows: auto 1fr;
      padding: 3rem 0;
    }
  }

  .logo {
    /* to be over .header::before */
    position: relative;

    align-self: start;
    display: flex;
    align-items: center;

    &__text {
      margin: 0;
      margin-left: 1em;

      /* align with logo icon */
      position: relative;
      top: 4px;
    }
  }

  .wrapper {    
    /* to be over .header::before */
    position: relative;
  }
</style>

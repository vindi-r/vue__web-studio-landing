<template lang="pug">
  section.services
    .inner.services__inner

      .wrapper
        h1.services__title Our services
        Divider.services__divider
        p.services__description.
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
          Aenean tincidunt sit amet erat malesuada interdum. 
          Aenean sodales dui quis leo fermentum scelerisque. 
          Fusce condimentum dolor 
          justo, ac tristique diam iaculis at.

      .tiles
        .tile
          .tile__content
            Notes
            h3.tile__title Project management
        
        .tile
          .tile__content
            Tools
            h3.tile__title crm customization
        
        .tile
          .tile__content
            Shield
            h3.tile__title seo/sem
        
        .tile
          .tile__content
            Chemical_glass
            h3.tile__title bussiness inteligence
        
        .tile
          .tile__content
            Layers
            h3.tile__title data normalization
        
        .tile
          .tile__content
            Antenna
            h3.tile__title digital marketing
        
        .tile
          .tile__content
            Chart
            h3.tile__title data acquision
        
        .tile
          .tile__content
            Bulb
            h3.tile__title product development
</template>

<script>

import Divider from '../Divider.vue';

// Icons
import Antenna from '../icons/Antenna.vue';
import Bulb from '../icons/Bulb.vue';
import Chart from '../icons/Chart.vue';
import Chemical_glass from '../icons/Chemical_glass.vue';
import Layers from '../icons/Layers.vue';
import Notes from '../icons/Notes.vue';
import Shield from '../icons/Shield.vue';
import Tools from '../icons/Tools.vue';

export default {
  components: {
    Divider,
    Antenna,
    Bulb,
    Chart,
    Chemical_glass,
    Layers,
    Notes,
    Shield,
    Tools
  }
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/vars';

  .services {
    display: grid;
    grid-template-columns: 1fr 1200px 1fr;
    background-color: $c-accent1;
    color: $c-secondary;

    &__inner {      
      align-items: center;
      display: grid;
      grid-template-columns: 500px 1fr;
      grid-column: 2 / 4;
    }

    &__title {
      text-transform: uppercase;
      margin-bottom: 0;
    }

    &__divider {
      background-color: $c-secondary;
      margin-top: 1rem;
    }

    &__description {
      color: $c-third;
    }
  }

  .wrapper {
    grid-column: 1 / 2;
    grid-row: 1 / 2;
  }

  .tiles {
    grid-column: 1 / 3;
    grid-row: 1 / 2;
    justify-self: end;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: .5rem;

    
    transform: rotate(45deg) translateX(10%) translateY(-10%);
    transform-origin: top left;
  }

  .tile {
    width: 200px;
    height: 200px;

    background-color: $c-main;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;

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

    &__content {
      transform: rotate(-45deg);
    }
    
    &__title {
      color: $c-secondary;
      text-transform: uppercase;
      font-size: .8em;
    }
  }

</style>



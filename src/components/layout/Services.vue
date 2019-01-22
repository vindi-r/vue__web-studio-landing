<template lang="pug">
  section.services
    .inner.services__inner

      .services__wrapper
        h1.services__title Our services
        Divider.divider_black
        p.services__description.
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
          Aenean tincidunt sit amet erat malesuada interdum. 
          Aenean sodales dui quis leo fermentum scelerisque. 
          Fusce condimentum dolor 
          justo, ac tristique diam iaculis at.

      //- .tiles
      //-   .tile
      //-     .tile__content
      //-       Notes
      //-       h3.tile__title Project management
        
      //-   .tile
      //-     .tile__content
      //-       Tools
      //-       h3.tile__title crm customization
        
      //-   .tile
      //-     .tile__content
      //-       Shield
      //-       h3.tile__title seo/sem
        
      //-   .tile
      //-     .tile__content
      //-       Chemical_glass
      //-       h3.tile__title bussiness inteligence
        
      //-   .tile
      //-     .tile__content
      //-       Layers
      //-       h3.tile__title data normalization
        
      //-   .tile
      //-     .tile__content
      //-       Antenna
      //-       h3.tile__title digital marketing
        
      //-   .tile
      //-     .tile__content
      //-       Chart
      //-       h3.tile__title data acquision
        
      //-   .tile
      //-     .tile__content
      //-       Bulb
      //-       h3.tile__title product development

      .tiles
        Tile(
          v-for="tile in tiles"
        ) {{ tile.icon }}
          h3.tile__title {{ tile.title }}

</template>

<script>

import Divider from '../Divider.vue';
import Tile from '../Tile.vue';

// Icons
import Antenna from '../icons/Antenna.vue';
import Bulb from '../icons/Bulb.vue';
import Chart from '../icons/Chart.vue';
import ChemicalGlass from '../icons/ChemicalGlass.vue';
import Layers from '../icons/Layers.vue';
import Notes from '../icons/Notes.vue';
import Shield from '../icons/Shield.vue';
import Tools from '../icons/Tools.vue';
import NotesVue from '../icons/Notes.vue';

export default {
  components: {
    Divider,
    Antenna,
    Bulb,
    Chart,
    ChemicalGlass,
    Layers,
    Notes,
    Shield,
    Tools,
    Tile
  },

  data: () => ({
    tiles: [
      {
        icon: Notes,
        title: 'Project management'
      },
      {
        icon: Tools,
        title: 'crm customization'
      },
      {
        icon: Shield,
        title: 'seo/sem'
      },
      {
        icon: ChemicalGlass,
        title: 'bussiness inteligence'
      },
      {
        icon: Layers,
        title: 'data normalization'
      },
      {
        icon: Antenna,
        title: 'digital marketing'
      },
      {
        icon: Chart,
        title: 'data acquision'
      },
      {
        icon: Bulb,
        title: 'product development'
      }
    ]
  })
}
</script>

<style lang="scss">
  @import '../../assets/style/vars';

  .services {
    display: grid;
    grid-template-columns: 1fr 1200px 1fr;
    background-color: $c-accent1;
    color: $c-secondary;
    overflow: hidden;

    padding: 4rem 0;

    @include bp($xxxl) {
      padding: 0;
    }

    &__inner {
      align-items: center;
      display: grid;
      grid-template-columns: 500px 1fr;
      grid-column: 2 / 4;
    }

    &__wrapper {
      grid-column: 1 / 2;
      grid-row: 1 / 2;
    }

    &__title {
      text-transform: uppercase;
      margin-bottom: 0;
      font-weight: bold;
    }

    &__description {
      color: $c-third;
    }
  }


  // .tiles {
  //   grid-column: 1 / 3;
  //   grid-row: 1 / 2;
  //   justify-self: end;
  //   display: grid;
  //   grid-template-columns: repeat(4, 1fr);
  //   grid-gap: .5rem;

    
  //   transform: rotate(45deg);
  //   transform-origin: center center;

  //   @include bp($xxl) {
  //     transform: rotate(45deg) translateX(-15%) translateY(15%);
  //   }

  //   @include bp($xxxl) {
  //     transform: rotate(45deg) translateX(-35%) translateY(25%);
  //     grid-template-columns: 1fr 1fr 1fr
  //   }
  // }

  // .tile {
  //   width: 180px;
  //   height: 180px;

  //   background-color: $c-main;
  //   display: flex;
  //   flex-direction: column;
  //   align-items: center;
  //   justify-content: center;
  //   text-align: center;
    
  //   &:nth-child(1) {
  //     grid-column-start: 2;
  //   }    
  //   &:nth-child(2) {
  //     grid-column-start: 1;
  //   }
  //   &:nth-child(5) {
  //     grid-column-start: 2;
  //   }
  //   &:nth-child(8) {
  //     grid-column-start: 3;
  //   }

  //   @include bp($xxxl) {
  //     &:nth-child(1) {
  //       grid-column-start: 3;
  //     }
  //     &:nth-child(2) {
  //       grid-column-start: 2;
  //     }
  //     &:nth-child(6) {
  //       grid-column-start: 1;
  //     }
  //     &:nth-child(8) {
  //       grid-column-start: 1;
  //     }
  //   }


  //   &__content {
  //     transform: rotate(-45deg);
  //   }
    
  //   &__title {
  //     color: $c-secondary;
  //     text-transform: uppercase;
  //     font-size: .7em;
  //     font-weight: bold;
  //   }
  // }

</style>



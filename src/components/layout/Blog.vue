<template lang="pug">
  section.blog
    .inner.blog__inner
      .wrapper
        h1.blog__title read our minds
        Divider.divider_black
      p.blog__description.
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
        Phasellus aliquet purus et orci tincidunt tempus. 
        Duis ultricies, nibh.

      table.posts
        thead.posts__header
          tr
            td(style="width: 60%")
              h3.posts__title.posts__title_main title &amp; desctiption
            
            td(style="width: 20%")
              h3.posts__title.posts__title_main date
            
            td(style="width: 20%")
              h3.posts__title.posts__title_main who
        tbody
          tr.posts__item
            td
              h3.posts__title Weekly Digital Roundup
              p.post__text.
                Wi-Fi apple care volume reminder controls. 
                My stations folders mac power ultimate upgrade. 
                Shop online quicktime trackpad server aperture rumors 
                education safari one to one.
            td
              h3.posts__title 08/12/2018
            td
              h3.posts__title Adam Campbell
          tr.posts__item
            td
              h3.posts__title Something new
              p.post__text.
                Backlit keyboard chess phone airport extreme 
                support iPad. Accessories magsafe terminal final 
                cut pro. Featured TV shows downloads digital color meter. 
            td
              h3.posts__title 07/12/2018
            td
              h3.posts__title Victor Csuka
          tr.posts__item
            td
              h3.posts__title things coming around
              p.post__text.
                Wi-Fi apple care volume reminder controls. 
                My stations folders mac power ultimate upgrade. 
                Shop online quicktime trackpad server aperture 
                rumors education safari one to one.
            td
              h3.posts__title 04/12/2018
            td
              h3.posts__title Vivek Ravin
          tr.posts__item
            td
              h3.posts__title finally! we are here
              p.post__text.
                Glossy tech specs bluetooth manuals. OpenGL products 
                FaceTime free shipping recycling mission control 
                applications.
            td
              h3.posts__title 01/12/2018
            td
              h3.posts__title Himket Arslan

</template>

<script>
import Divider from '../Divider'

export default {
  name: 'Blog',

  components: {
    Divider
  }
}
</script>

<style lang="scss">
  @import '../../assets/style/vars';

  .blog {
    display: grid;
    grid-template-columns: 1fr 1200px 1fr;
    padding: 8rem 0;

    &__inner {
      display: grid;
      grid-template-columns: auto 1fr;
      grid-gap: 0 5rem;
    }

    &__title {
      font-weight: bold;
      text-transform: uppercase;
    }

    &__description {
      // to align with title
      margin-top: .5rem;

      max-width: 500px;
      color: $c-third;
    }
  }

  .posts {
    font-size: .8em;
    grid-column: 1 / -1;

    &__header {
      border-bottom: 1px solid rgba($c-secondary, .2);
    }

    &__item {
      border-bottom: 1px solid rgba($c-secondary, .2);
      
      &:hover {
        background: $c-secondary;
        color: $c-main;
      }
      
      & td {
        padding: 2rem 0;

        &:first-child {
          padding: 2rem;
          padding-right: 6rem;
        }
      }
    }

    &__title {
      margin-bottom: 1.5rem;
      font-size: 1.2em;
      text-transform: uppercase;

      &_main {
        margin-bottom: 1rem;
        color: lighten($c-third, 6.5%);
      }
    }

    &__text {
      color: $c-secondary;
    }
  }
</style>


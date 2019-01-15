<template>
  <header class="header">
    <div class="inner header__inner">
      <div class="logo">
        <Briefcase/>
        <p class="logo__text">Logo goes here</p>       
      </div>

      <div class="wrapper">

        <h1>So begins a new age 
          <br>
          of knowledge
        </h1>

        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vitae nulla quis 
          <br>
          turpis cursus pharetra. Fusce blandit nec tortor sit amet ullamcorper.
        </p>
        
        <Divider />

        <Button v-text="title"/>
      
      </div>
    </div>

  </header>
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

<style>
  .header {
    height: 100vh;
    max-height: 900px;
    color: #fff;

    /* for ::before */
    position: relative;
  }

  .header::before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;

    background-image: url('../../assets/banner.png');
    background-size: cover;
    background-position: center center;
    filter: brightness(60%)
  }



  .header__inner {
    height: 100%;
    display: grid;
    align-items: center;
    grid-template-rows: auto 1fr;
    padding: 3rem 1rem;
  }

  .logo {
    /* to be over .header::before */
    position: relative;

    align-self: start;
    display: flex;
    align-items: center;
  }

  .logo__text {
    margin: 0;
    margin-left: 1em;

    /* align with logo icon */
    position: relative;
    top: 4px;
  }

  .wrapper {    
    /* to be over .header::before */
    position: relative;
  }
</style>

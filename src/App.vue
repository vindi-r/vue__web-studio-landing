<template lang="pug">
  #app
    Header
    Services
    Works
    Projects
</template>

<script>
import Header from './components/layout/Header.vue';
import Services from './components/layout/Services.vue';
import Works from './components/layout/Works.vue';
import Projects from './components/layout/Projects.vue';

export default {
  name: 'app',
  components: {
    Header,
    Services,
    Works,
    Projects
  }
}
</script>

<style lang="scss">

/* RESET */
/* http://meyerweb.com/eric/tools/css/reset/
 * v2.0 | 20110126
 * License: none (public domain) */
 html, body, div, span, applet, object, iframe,
 h1, h2, h3, h4, h5, h6, p, blockquote, pre, a,
 abbr, acronym, address, big, cite, code, del,
 dfn, em, img, ins, kbd, q, s, samp, small, strike,
 strong, sub, sup, tt, var, b, u, i, center,
 dl, dt, dd, ol, ul, li, fieldset, form, label,
 legend, table, caption, tbody, tfoot, thead,
 tr, th, td, article, aside, canvas, details, embed,
 figure, figcaption, footer, header, hgroup, menu,
 nav, output, ruby, section, summary, time, mark,
 audio, video {
   margin: 0;
   padding: 0;
   border: 0;
   font-size: 100%;
   font: inherit;
   vertical-align: baseline;
 }
 
 /* HTML5 display-role reset for older browsers */
 article, aside, details, figcaption, figure,
 footer, header, hgroup, menu, nav, section {
   display: block;
 }


@import url('https://fonts.googleapis.com/css?family=Roboto:300,400,700');

@import './assets/style/vars';

body {
  line-height: 1.25;
  font-family: 'Roboto', sans-serif;
  font-size: 14px;

  @include bp($md) {
    font-size: 16px;
  }

  @include bp($lg) {
    font-size: 18px;
  }

  @include bp($xxl) {
    font-size: 20px;
  }
}

h1 {
  font-size: 3.5em;
  margin-bottom: 2rem;
}

h2 {
  font-size: 1.8em;
}

h3 {
  font-size: 1.5em;
}

p {
  margin-bottom: 1rem;
  font-weight: 300;
  line-height: 1.5;
}


 
ol, ul {
  list-style: none;
}

blockquote, q {
  quotes: none;
}

blockquote:before, blockquote:after, q:before, q:after {
  content: "";
  content: none;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}
/* RESET END */

.inner {
  box-sizing: border-box;
  grid-column-start: 2;
  // max-width: 1200px;
  // margin: auto;
  // padding-left: 1rem;
  // padding-right: 1rem;
}
</style>

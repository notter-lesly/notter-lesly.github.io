<template>
  <div>
    <TheHeader @event="scrollDown" />
    <main>
      <slot />
    </main>
    <TheFooter id="footer" />
  </div>
</template>

<script setup lang="ts">
  function scrollDown() {
    const footer = document.querySelector("#footer");
    footer.scrollIntoView();
  }
</script>

<style>
  html,
  body,
  div,
  span,
  applet,
  object,
  iframe,
  h1,
  h2,
  h3,
  h4,
  h5,
  h6,
  p,
  blockquote,
  pre,
  a,
  abbr,
  acronym,
  address,
  big,
  cite,
  code,
  del,
  dfn,
  em,
  img,
  ins,
  kbd,
  q,
  s,
  samp,
  small,
  strike,
  strong,
  sub,
  sup,
  tt,
  var,
  b,
  u,
  i,
  center,
  dl,
  dt,
  dd,
  ol,
  ul,
  li,
  fieldset,
  form,
  label,
  legend,
  table,
  caption,
  tbody,
  tfoot,
  thead,
  tr,
  th,
  td,
  article,
  aside,
  canvas,
  details,
  embed,
  figure,
  figcaption,
  footer,
  header,
  hgroup,
  menu,
  nav,
  output,
  ruby,
  section,
  summary,
  time,
  mark,
  audio,
  video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
  }

  /* HTML5 display-role reset for older browsers */
  article,
  aside,
  details,
  figcaption,
  figure,
  footer,
  header,
  hgroup,
  menu,
  nav,
  section {
    display: block;
  }

  body {
    line-height: 1;
  }

  ol,
  ul {
    list-style: none;
  }

  blockquote,
  q {
    quotes: none;
  }

  blockquote:before,
  blockquote:after,
  q:before,
  q:after {
    content: none;
  }

  table {
    border-collapse: collapse;
    border-spacing: 0;
  }

  main {
    display: grid;
    grid-template-columns: 2rem 6rem auto 6rem 2rem;
    grid-template-rows: 7rem auto;
    min-height: 85vh;
    background-color: #dfcfd5;
  }

  .router-link-active .router-link-exact-active {
    background-color: pink;
  }

  .sub-title {
    font-size: 1.3rem;
    text-align: center;
    font-family: "karla";
    padding-bottom: 1rem;
  }

  p {
    line-height: 1.4rem;
    font-family: "spectral", "roboto";
    padding: 0.2rem 0 0.5rem 0;
  }

  h2 {
    font-family: "karla";
    font-size: 0.8rem;
    padding: 1rem 0 0 0;
  }
</style>

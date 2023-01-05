<script setup lang="ts">
function scrollDown() {
  const footer = document.querySelector('#footer')
  footer.scrollIntoView()
}
</script>

<template>
  <div if()>
    <TheHeader @event="scrollDown" />
    <main>
      <slot />
    </main>
    <TheFooter id="footer" />
  </div>
</template>

<style lang="scss">
main {
  display: grid;
  grid-template-columns: 2rem 6rem auto 6rem 2rem;
  grid-template-rows: 7rem auto;
  min-height: 85vh;
  background-color: #dfcfd5;

  @include for-tablet-landscape-up {
    display: grid;
    grid-template-columns: 2rem 6rem 12rem auto 12rem 6rem 2rem;
    grid-template-rows: 7rem 9rem auto;
    background-color: rgb(11, 11, 11);
    background-size: 100%;
  }
}
</style>

<script setup lang="ts"></script>

<template>
  <div if()>
    <TheHeader />
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
  background-color: rgb(11, 11, 11);

  @include for-tablet-landscape-up {
    display: grid;
    grid-template-columns: 2rem 6rem 12rem auto 12rem 6rem 2rem;
    grid-template-rows: 7rem 9rem 5rem auto;
    background-size: 100%;
  }
}
</style>

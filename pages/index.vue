<script setup lang="ts">
const picture = new URL('../assets/about.jpeg', import.meta.url).href
</script>

<template>
  <div id="index">
    <h1 class="wave">Hello, I am Lesly!</h1>
    <img class="image" :src="picture" />
  </div>
</template>

<style lang="scss">
#index {
  grid-column: 2/5;
  grid-row: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
  @include for-tablet-landscape-up {
    justify-content: flex-start;
    grid-column: 3/6;
    grid-row: 3/-1;
    gap: 3rem;
  }
}
.wave {
  font-family: $main-font;
  font-size: 2rem;
  color: white;
}

.image {
  max-width: 10rem;
  width: 6rem;
  padding: 1rem;
  border-radius: 20%;
  @include for-tablet-landscape-up {
    max-width: 9rem;
    width: auto;
  }
}
</style>

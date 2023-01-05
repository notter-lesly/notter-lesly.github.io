<script setup lang="ts">
const picture = new URL('../assets/about.jpeg', import.meta.url).href
</script>

<template>
  <img class="image" :src="picture" />

  <h1>Welcome!!</h1>
</template>

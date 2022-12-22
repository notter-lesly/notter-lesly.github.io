<template>
  <div id="about">
    <h1 class="sub-title">About Me</h1>
    <div class="flex">
      <img
        class="image"
        :src="picture" />
      <ul class="about-text">
        <li
          v-for="phrases in aboutMe"
          :key="phrases.key">
          <p>{{ phrases.value }}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
  const picture = new URL("../assets/about.jpeg", import.meta.url).href;
  const aboutMe = [
    {
      value:
        "My name is Lesly Notter dos Anjos and I am a Frontend Developer based in the Netherlands",
      key: 0,
    },
    {
      value:
        "I have a bachelor degree in information systems and 1 year of experience as a frontender",
      key: 1,
    },
  ];
</script>

<style scoped>
  #about {
    grid-column: 2/5;
    grid-row: 2;
    justify-content: center;
  }

  .about-text {
    padding: 1rem 0;
    margin-bottom: 1rem;
  }

  .flex {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .image {
    max-width: 7rem;
    padding: 1rem;
    border-radius: 20%;
  }

  .menu-decoration-left {
    width: 15rem;
    height: 5rem;
    position: absolute;
    border: 1px solid white;
    align-self: center;
    grid-row: 4;
    z-index: 1;
    border-left: none;
    border-radius: 20%;
    opacity: 0.5;
    transform: rotate(45deg);
  }
  .menu-decoration-right {
    width: 15rem;
    height: 5rem;
    position: absolute;
    border: 1px solid white;
    align-self: center;
    grid-column: 3/5;
    grid-row: 6;
    z-index: 1;
    border-left: none;
    border-radius: 20%;
    opacity: 0.5;
    transform: rotate(-45deg);
  }
</style>

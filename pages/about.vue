<template>
  <div id="about">
    <h1 class="sub-title">About Me</h1>
    <div class="flex">
      <img
        class="image"
        :src="picture" />
      <div class="name">
        <h1 class="about-title">Lesly Notter</h1>
        <h3 class="about-subtitle">Front End Developer</h3>
      </div>
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
  }

  .flex {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .image {
    max-width: 8rem;
    padding: 1rem;
    border-radius: 20%;
  }

  .about-title {
    font-size: 1.1rem;
    font-family: "spectral";
    padding-bottom: 0.5rem;
    text-align: center;
  }

  .about-subtitle {
    font-size: 0.8rem;
    font-family: "spectral";
    font-weight: 400;
  }

  .name {
    display: flex;
    align-items: center;
    flex-direction: column;
  }
</style>

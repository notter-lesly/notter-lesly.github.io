<script setup lang="ts">
const secondExperience = false
const experiences = [
  {
    company: 'Cm.com',
    time: '02/2022 - 02/2023',
    description1: 'Website: Adding new features and fixing bugs.',
    description2:
      'Management system: rebuild from scratch with TypeScript and Nuxt.',
    tech: 'Html, CSS/Sass, Javascript, Typescript, Vue3, Nuxt3, Vite, Cypress, Docker',
    tools: 'Gitlab, sketch, invision, Agil/Scrum',
    key: 0,
  },
]
</script>

<template>
  <ul>
    <li v-for="experience in experiences" :key="experience.key">
      <p class="company">{{ experience.company }}</p>
      <p class="time">{{ experience.time }}</p>
      <p>{{ experience.description1 }}</p>
      <p>{{ experience.description2 }}</p>
      <p class="tools">Tools/Technologies used:</p>
      <p>{{ experience.tech }}</p>
      <p>{{ experience.tools }}</p>
    </li>
  </ul>
</template>

<style scoped lang="scss">
.company {
  @include titles;
  font-size: 1rem;
}

.time {
  @include sub-title;
}

.tools {
  font-weight: bold;
}
</style>

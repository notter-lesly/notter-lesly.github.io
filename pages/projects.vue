<script setup lang="ts">
const experiences = [
  {
    company: 'Digital Society School(AUAS)',
    time: '09/2021 - 01/2022',
    description1:
      'Create a product to solve the problem: e-assessment of students practical skills.',
    description2:
      'the whole process chain: analysis, brainstorming, ux research, ui, design, etc',
    tools:
      'Agil/Scrum, Design thinking, Figma, AdobeXD, Ui, Uxresearch, Usertest',
    key: 0,
  },
  {
    company: 'Cm.com',
    time: '02/2022 - 02/2023',
    description1: 'Website: Adding new features and fixing bugs.',
    description2:
      'Management system: rebuild from scratch with TypeScript and Nuxt.',
    tech: 'Html, CSS/Sass, Javascript, Typescript, Vue3, Nuxt3, Vite, Cypress, Docker',
    tools: 'Gitlab, sketch, invision, Agil/Scrum',
    key: 1,
  },
]
</script>

<template>
  <section id="project">
    <h1 class="sub-title">Experiences</h1>
    <ul>
      <li v-for="experience in experiences" :key="experiences.key">
        <p class="company">{{ experience.company }}</p>
        <p class="time">{{ experience.time }}</p>
        <p>{{ experience.description1 }}</p>
        <p>{{ experience.description2 }}</p>
        <p class="tools">Tools/Technologies used:</p>
        <p>{{ experience.tech }}</p>
        <p>{{ experience.tools }}</p>
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped>
#project {
  grid-column: 2/5;
  grid-row: 2;

  @include for-tablet-landscape-up {
    grid-column: 3/6;
    grid-row: 3;
    z-index: 2;
    color: white;
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
  }

  ul {
    display: flex;
    justify-content: space-between;
  }
}

.company {
  font-size: 1rem;
  font-family: '$main-font';
  padding-bottom: 0.3rem;
  font-weight: bold;
}

.time {
  font-size: 0.8rem;
  font-family: 'roboto';
  padding-bottom: 0.2rem;
}

li {
  padding-bottom: 0.5rem;
  @include for-tablet-landscape-up {
    word-wrap: break-word;
    max-width: 40%;
  }
}

.tools {
  font-weight: bold;
}
</style>

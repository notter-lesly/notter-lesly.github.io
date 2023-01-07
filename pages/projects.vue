<script setup lang="ts">
const cmExperience = ref(true)

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
    <h1 class="title">Experiences</h1>
    <div class="mobile-experience">
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
    </div>
    <div class="desktop-experience">
      <div class="experience-buttons">
        <Button @click="cmExperience = false" button-text=" DSS" />
        <Button @click="cmExperience = true" button-text="Cm" />
      </div>
      <Cm v-if="cmExperience" />
      <Dss v-if="!cmExperience" />
    </div>
  </section>
</template>

<style scoped lang="scss">
#project {
  grid-column: 2/5;
  grid-row: 2;
  color: azure;

  @include for-tablet-landscape-up {
    grid-column: 3/6;
    grid-row: 3/-1;
    z-index: 2;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    .title {
      margin-bottom: 1rem;
    }
  }
}

.company {
  font-family: $main-font;
  font-weight: bold;
}

.time {
  font-size: 0.8rem;
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
.mobile-experience {
  display: block;
  @include for-tablet-landscape-up {
    display: none;
  }
}
.desktop-experience {
  display: none;
  @include for-tablet-landscape-up {
    display: flex;
    flex-direction: column;
    align-self: center;
    gap: 1rem;
  }
  .experience-buttons {
    display: flex;
    justify-content: center;
    gap: 5rem;
    Button {
      min-width: 3rem;
    }
    :focus,
    :active {
      background-color: $focus-color;
    }
  }
}
</style>

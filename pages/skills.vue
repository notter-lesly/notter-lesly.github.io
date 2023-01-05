<template>
  <div id="skills">
    <h1 class="sub-title">My skills</h1>
    <ul class="skills-list">
      <li class="skill" v-for="skill in skills" key="skill.key">
        {{ skill.value }}
        <Measure :skillMeasure="skill.measure" />
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
const skills = [
  { value: 'Html:', key: 0, measure: '7rem' },
  { value: 'Css/Sass:', key: 1, measure: '7rem' },
  { value: 'JavaScript:', key: 2, measure: '6rem' },
  { value: 'Vue3:', key: 3, measure: '6rem' },
  { value: 'Nuxt3:', key: 4, measure: '5rem' },
  { value: 'Typescript:', key: 5, measure: '4rem' },
]

const tools = [
  {
    value:
      'Tools: VS Code, Docker, Figma, InVision, Eslint, Prettier, Postman, Gitlab ',
    key: 1,
  },
]
</script>

<style lang="scss" scoped>
#skills {
  grid-column: 2/5;
  grid-row: 2;

  @include for-tablet-landscape-up {
    z-index: 2;
    grid-column: 4/5;
    grid-row: 4;
    color: white;
  }
}

.skills-list {
  font-family: 'roboto';
  font-size: 1rem;
  margin-top: 1rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  justify-content: space-between;
}

.skill {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>

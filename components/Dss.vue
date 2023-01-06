<script setup lang="ts">
const secondExperience = false
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
      <p>{{ experience.tools }}</p>
    </li>
  </ul>
</template>

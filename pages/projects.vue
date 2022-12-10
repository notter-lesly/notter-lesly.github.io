<template>
  <section id="project">
      <h1 class="sub-title">Experiences</h1>
      <ul>
        <li v-for=" experience in experiences" :key="experiences.key">
        <p class="company"> {{ experience.company }} </p>
        <p class="time"> {{experience.time}}</p>
        <p > {{experience.description}}</p>
        <b>Tools/Technologies used:</b> <p> {{experience.tech }}</p>
      <p> {{experience.tools }}</p>   
 
        </li>
      </ul>
    </section>
    
    
    </template>

<script setup>


const experiences =[
{'company': 'Digital Society School(AUAS)',
 'time': '09/2021 - 01/2022',
 'description':'In this traineeship, I worked on a project about the e-assessment of students practical skills with Erasmus, Inter-Cultural, Universitat autònoma de Barcelona and West University of Timisoara. I also participated in various workshops on design thinking, design in general and technology.',
 'tools': 'Agil/Scrum, Design thinking, Figma, AdobeXD, Ui, Uxresearch, Usertest',
 'key': 0},
{'company': 'Cm.com',
 'time': '02/2022 - 02/2023',
 'description': 'At CM I worked with maintaining, adding new features and fixing bugs to our own Website and to our Content Management System (CMS). I also helped in a major update to our CMS frontend, where we were fully rebuilding our frontend from scratch using TypeScript and Nuxt.',
 'tech':'Html, CSS/Sass, Javascript, Typescript, Vue3, Nuxt3, Vite, Cypress, Docker',
 'tools': 'Gitlab, sketch, invision, Agil/Scrum',
 'key':1},
]
</script>

<style scoped>

#project{
    grid-column: 2/5;
    grid-row: 2;
}
.company{
  font-size: 1rem;
  font-family: 'karla';
  padding-bottom: 0.3rem;
  font-weight: bold;
}
.time{
  font-size: 0.8rem;
  font-family: 'roboto';
  padding-bottom: 0.2rem;
}

li{
  padding-bottom: 0.5rem;
}
</style>
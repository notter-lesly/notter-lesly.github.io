<template>
    <div id="skills">
    <h1 class="sub-title"> My skills </h1>
    <ul class=skills-list v-for="skill in skills" key="skill.key">
        <li>
            {{skill.value}}
        </li>
        <Measure
        :skillMeasure="skill.measure"/>
    </ul>
</div>
</template>


<script setup lang="ts">

const skills = [{'value' : 'Html','key': 0, 'measure':"4rem"},
                {'value' : 'Css/Sass','key': 1, 'measure':"4rem"}, 
                {'value' : 'JavaScript','key': 2, 'measure':"3rem"}, 
                {'value' : 'Vue3','key': 3, 'measure':"3rem"}, 
                {'value' : 'Nuxt3','key': 4, 'measure':"2rem"},
                {'value' : 'Typescript','key': 5, 'measure':"1rem"},
                ]

const tools= [{'value' : 'Tools: VS Code, Docker, Figma, InVision, Eslint, Prettier, Postman, Gitlab ', 'key': 1}]

</script>

<style scoped>
#skills{
    grid-column: 2/5;
    grid-row: 2;
}

.skills-list{
    font-family: 'roboto';
    font-size: 1rem;
    margin-top: 1rem;
}

</style>
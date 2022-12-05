<template>
<div id="about">
    <h1 class="title">About Me</h1>
<div  class="flex">

<img class= "image" :src="picture">
<ul>
<li v-for="phrases in aboutMe" :key="phrases.key" class="text"> {{phrases.value}}</li>
</ul> 

</div>
</div>


</template>

<script setup lang="ts">

const picture = new URL('../assets/about.jpeg', import.meta.url).href
const aboutMe = [{'value' : 'My name is Lesly Notter dos Anjos and I am a Frontend Developer based in the Netherlands', 'key': 0},
                 {'value' : 'I have a bachelor degree in information systems and 1 year of experience as a frontender', 'key': 1},
                ]


</script>

<style scoped>

#about{
    grid-column: 2/5;
    justify-content: center;
    margin: 1rem 0 1rem 0;
}

.flex{
    display:flex;
    flex-direction:column; 
    align-items: center;
}

.image{
max-width: 8rem;
padding:1rem;
border-radius: 20%;
}

.text{ 
   line-height:1.4rem;
   padding: 0.2rem;

}
.title{
    font-size: 20px;
    text-align: center;
    padding:6px;
  }

</style>
<template>
  <section id="project">
      <h1>Projects</h1>
      <ul>
        <li v-for="slide in mySlides" :key="mySlides.key">
        <h1> {{ slide.name }}</h1>
        <img :src="slide.url"/>
        
        </li>
      </ul>

        <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
        <a class="next" onclick="plusSlides(1)">&#10095;</a>
     
      <br />

    </section>
    
    
    </template>

<script setup>


const mySlides =[
{'name': 'animals', 'url': new URL('../assets/animals.jpg', import.meta.url).href, 'key': 0},
{'name': 'dog', 'url': new URL('../assets/dog.jpg', import.meta.url).href, 'key': 1},
{'name': 'orphanage', 'url': new URL('../assets/orphanage.jpg', import.meta.url).href, 'key': 2},
{'name': '', 'url': new URL('../assets/store.jpg', import.meta.url).href, 'key': 3},

]
</script>

<style scoped>

#project{
    grid-column: 2/5;
}
img{
    width: 100%
}

.dots{
 text-align: center;
}

</style>
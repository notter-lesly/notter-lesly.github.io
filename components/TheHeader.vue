<template>
    <div class="header">
        <h1 class="title"> Lesly Notter</h1>
        <h3 class="subtitle"> Front End Developer</h3>
    </div>
    <nav class="menu">
    <nuxtLink to="/About"> About </nuxtLink>
    <nuxtLink to="/skills"> Skills </nuxtLink>
    <nuxtLink to="/projects"> Projects </nuxtLink>
    <a @click="scrollFooter"> Contact  </a>
    </nav>
</template>

<script setup>

const emit = defineEmits(['event'])

function scrollFooter(){
   emit('event')
}
</script>
<style scoped>

.header{
    display: flex;
    align-items: center;
    flex-direction: column;
    }

.title{
    font-size:20px;
    margin: 1rem 0 1rem 0;
    font-family: 'Tangerine';
}

.subtitle{
    font-size:16px;
    margin: 0.5rem 0 1rem 0;
}

a.nuxt-link{
    color:black;
}

a.nuxt-link-active{
    color:blueviolet;
}

.menu{
    display: flex;
    justify-content: space-around;
} 

.menu a{
    cursor:pointer;
    text-decoration: underline;
}


</style>
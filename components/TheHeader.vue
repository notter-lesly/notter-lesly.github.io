<template>
    <div class="theHeader">
    <div class="name">
        <h1 class="header-title"> Lesly Notter</h1>
        <h3 class="header-subtitle"> Front End Developer</h3>
    </div>
    <nav class="menu">
        <nuxtLink to="/about"><Button :button-text="about"> </Button></nuxtLink>
        <nuxtLink to="/skills"><Button :button-text="skills"> </Button></nuxtLink>
        <nuxtLink to="/projects"><Button :button-text="projects"> </Button></nuxtLink>
        <a @click="scrollFooter"><Button :button-text="contact"> </Button></a>
    </nav>
</div>
</template>

<script setup lang="ts">

//Consts
const about="About"
const skills="skills"
const projects="experience"
const contact="contacts"
const emit = defineEmits(['event'])


//functions
function scrollFooter(){
   emit('event')
}
</script>
<style scoped>

.theHeader{

background-color: #AAB1C3;
width: 100%;
}


.name{
    display: flex;
    align-items: center;
    flex-direction: column;

    }

.header-title{
    font-size:1.3rem;
    margin: 1rem 0 0 0;
    font-family: 'karla';
    padding:12px;
    text-align: center;
}

.header-subtitle{
    font-size:1rem;
    margin: 0 0 1rem 0;
    font-family: 'spectral';
    font-weight: 400;
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
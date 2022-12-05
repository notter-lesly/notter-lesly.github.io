<template>
    <div class="theHeader">
    <div class="name">
        <h1 class="title"> Lesly Notter</h1>
        <h3 class="subtitle"> Front End Developer</h3>
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
const projects="projects"
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

.title{
    font-size:20px;
    margin: 1rem 0 0 0;
    font-family: 'Tangerine';
    padding:12px;
    text-align: center;
}

.subtitle{
    font-size:16px;
    margin: 0 0 1rem 0;
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
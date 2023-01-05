<script setup lang="ts">
//Consts
const about = 'About'
const skills = 'skills'
const projects = 'experience'
const contact = 'contacts'
const emit = defineEmits(['event'])
const menu = ref<boolean>(false)
const desktop = false
const picture = new URL('../assets/me.png', import.meta.url).href

//functions
function scrollFooter() {
  emit('event')
}

function openMenu() {
  menu.value = !menu.value
}
</script>

<template>
  <div class="theHeader">
    <svg
      class="menu"
      @click="openMenu"
      width="24px"
      height="24px"
      viewBox="0 0 24 24"
      version="1.1"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
    >
      <title>menu</title>
      <g
        stroke="none"
        stroke-width="1"
        fill="none"
        fill-rule="evenodd"
        class="Icons"
      >
        <g fill="currentColor" class="menu">
          <path
            d="M18,18 L6,18 C5.447,18 5,17.552 5,17 C5,16.448 5.447,16 6,16 L18,16 C18.553,16 19,16.448 19,17 C19,17.552 18.553,18 18,18 M18,13 L6,13 C5.447,13 5,12.552 5,12 C5,11.448 5.447,11 6,11 L18,11 C18.553,11 19,11.448 19,12 C19,12.552 18.553,13 18,13 M18,8 L6,8 C5.447,8 5,7.552 5,7 C5,6.448 5.447,6 6,6 L18,6 C18.553,6 19,6.448 19,7 C19,7.552 18.553,8 18,8"
            id="Fill-102"
          ></path>
        </g>
      </g>
    </svg>
    <Transition name="slide-down">
      <div v-show="menu">
        <div class="menu-mobile">
          <div class="name">
            <h1 class="about-title">Lesly Notter</h1>
            <h3 class="about-subtitle">Front End Developer</h3>
          </div>
          <svg
            class="menu"
            @click="openMenu"
            xmlns="http://www.w3.org/2000/svg"
            width="12"
            height="13"
            viewBox="0 0 12 13"
            fill="white"
          >
            <line
              y1="-0.5"
              x2="16.0534"
              y2="-0.5"
              transform="matrix(0.68483 -0.728703 0.551828 0.833958 1.00616 12.6981)"
              stroke="#D7D7D7"
            />
            <line
              y1="-0.5"
              x2="16.0534"
              y2="-0.5"
              transform="matrix(0.68483 0.728703 -0.551828 0.833958 0 1)"
              stroke="#D7D7D7"
            />
          </svg>
          <ul class="menu-mobile-links">
            <li>
              <nuxtLink to="/about" @click="openMenu"> About </nuxtLink>
            </li>
            <li>
              <nuxtLink to="/skills" @click="openMenu"> skills </nuxtLink>
            </li>
            <li>
              <nuxtLink to="/projects" @click="openMenu"> Experience </nuxtLink>
            </li>
          </ul>
          <div class="menu-decoration-left" />
          <div class="menu-decoration-right" />
        </div>
      </div>
    </Transition>
    <div class="name">
      <h1 class="about-title">Lesly Notter</h1>
      <h3 class="about-subtitle">Front End Developer</h3>
    </div>

    <div class="desktop">
      <nav class="menu-links">
        <nuxtLink to="/about"><Button :button-text="about"> </Button></nuxtLink>
        <nuxtLink to="/skills"
          ><Button :button-text="skills"> </Button
        ></nuxtLink>
        <nuxtLink to="/projects">
          <Button :button-text="projects"> </Button>
        </nuxtLink>
        <a @click="scrollFooter" class="scroll-footer"
          ><Button :button-text="contact"> </Button
        ></a>
      </nav>
    </div>
  </div>
</template>

<style scoped lang="scss">
.theHeader {
  background-color: #aab1c3;
  width: 100%;
  box-shadow: 0 0 5px 0 rgb(16 30 30 / 10%), 0 0 7px 0 rgb(16 30 30 / 15%),
    0 0 9px 0 rgb(16 30 30 / 10%);
  position: fixed;
  height: 72px;
  display: grid;
  grid-template-columns: 1.5rem 6rem auto 6rem 1.5rem;
  grid-template-rows: 2rem 1rem 6rem auto;

  @include for-tablet-landscape-up {
    height: 30%;
    width: 100%;
    background-image: url('../assets/background.png');
    background-repeat: no-repeat;
    background-size: 100%;
    object-fit: fill;
    border-bottom-right-radius: 80%;
    border-bottom-left-radius: 80%;
    z-index: 0;
  }
}

.desktop {
  display: none;
  @include for-tablet-landscape-up {
    display: flex;
    width: 100%;
    grid-column: 1/-1;
    grid-row: 1/-1;
    flex-direction: row;
  }
}
a.nuxt-link {
  color: rgb(221, 221, 221);
}
.menu {
  grid-column: 2;
  display: flex;
  align-self: center;
  grid-row: 2;
}
.menu-mobile {
  width: 100%;
  background-color: #aab1c3;
  position: absolute;
  height: 100vh;
  display: grid;
  grid-template-columns: 1.5rem 6rem auto 6rem 1.5rem;
  grid-template-rows: 2rem 1rem 3rem 10rem 10rem auto;
}

.menu-mobile-links {
  display: flex;
  justify-content: space-around;
  flex-direction: column;
  gap: 1rem;
  position: relative;
  grid-column: 2/5;
  grid-row: 4;
}

.menu-mobile li {
  border-bottom: 1px solid #c7d5e2;
  width: 100%;
  padding: 1rem 0;
}

.menu-mobile-links a {
  cursor: pointer;
  color: white;
  text-decoration: none;
  font-size: 20px;
  font-family: 'karla';
}
.about-title {
  font-size: 1.1rem;
  font-family: 'spectral';
  padding-bottom: 0.5rem;
  text-align: center;
  align-self: stretch;
  color: azure;
}

.about-subtitle {
  font-size: 0.8rem;
  font-family: 'spectral';
  font-weight: 400;
}

.name {
  display: flex;
  align-items: flex-end;
  flex-direction: column;
  grid-column: 3/5;
  justify-content: center;
  text-align: initial;
  grid-row: 2;
}

.background-styling {
  background-color: pink;
}

.menu-decoration-left {
  width: 15rem;
  height: 5rem;
  position: absolute;
  border: 1px solid white;
  align-self: center;
  grid-row: 4;
  z-index: 1;
  border-left: none;
  border-radius: 20%;
  opacity: 0.5;
  transform: rotate(45deg);
}
.menu-decoration-right {
  width: 15rem;
  height: 5rem;
  position: absolute;
  border: 1px solid white;
  align-self: center;
  grid-column: 3/5;
  grid-row: 6;
  z-index: 1;
  border-left: none;
  border-radius: 20%;
  opacity: 0.5;
  transform: rotate(-45deg);
}

.name {
  display: flex;
  align-items: center;
  flex-direction: column;
}

.header-title {
  font-size: 1.3rem;
  margin: 1rem 0 0 0;
  font-family: 'karla';
  padding: 12px;
  text-align: center;
}

.header-subtitle {
  font-size: 1rem;
  margin: 0 0 1rem 0;
  font-family: 'spectral';
  font-weight: 400;
}

a.nuxt-link {
  color: black;
}

.router-link-active .linkButton {
  background-color: palevioletred;
}
.menu-links {
  display: flex;
  align-items: flex-end;
  justify-content: space-around;
  flex-direction: row;
  width: 100%;
  align-items: center;
}

.menu a {
  cursor: pointer;
  text-decoration: underline;
}
</style>
